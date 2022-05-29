For Rails applications running over Postgresql many times different sessions are running simultaneously.

Droppint the database in this situation might not work.

Simple fix:

# Step 1

Get a list of all postgres connections with `ps -ef | grep postgres`

The list will look like this:

```
502   560   553   0 Thu08am ??         0:00.69 postgres: checkpointer process             
502   565   553   0 Thu08am ??         0:00.06 postgres: bgworker: logical replication launcher
502 45605   553   0  2:23am ??         0:00.01 postgres: st myapp_development [local] idle 
```

# Step 2

Stop whatever connection you want with sudo kill -9 <pid>, where pid is the value in the second column. 

In my case, I wanted to stop the last row, with pid 45605, so I use:
  
```
sudo kill -9 45605
```
