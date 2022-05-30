# How to move a commit to another branch in git


1. Take a note of the hash want to move, and start at master:

```
git checkout master
```

2. Make a new branch feature-b to put it on and check it out:
```
git checkout -b feature-b
```

3. Cherry pick the commit we want to move into the new branch to add just that commit to feature-b:

```
git checkout feature-b
git cherry-pick a1b2c3d
```

4. Reset feature-a branch back to the previous commit hash (say z1b2c3d). 

```
git checkout feature-a
git reset --hard z1b2c3d
```

Using git reset --hard will remove all the commit referencing the changes, and all the changes themselves, 
from feature-a branch, while leaving that commit on feature-b:
