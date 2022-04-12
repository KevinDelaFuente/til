---
layout: post
Title: Intro to Git and Scaffold
---

##Git
- 
| **Action** | **Git Command** | **Example** |
  |:----------|:--------------|:------|
  | git init | Initialize a repository |  |
  | git add -A | Adds files to be commited | |
  | git commit -m "Title" | Commits snapshot |

##Scaffold
- Scaffold will generate a migration file, we should alway check it does what we want before migrating it 
- Scaffols will use ProgreSQL instead of SQLite
##Rails
- 
- `rails db:migrate` will run the database
- `rails db:drop` will destroy the database, very risky
- `rails db:rollback` will eliminate the _last_ migration only


