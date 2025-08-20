# Git Exercises
# Git history
## Bundle 1
## Exercise 1
```bash

PS D:\old\The Gym\git-exercises> git init
Initialized empty Git repository in D:/old/The Gym/git-exercises/.git/
PS D:\old\The Gym\git-exercises> echo "Hello world" >> file.txt
PS D:\old\The Gym\git-exercises> git config --global --add safe.directory 'D:/old/The Gym/git-exercises'
PS D:\old\The Gym\git-exercises> git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        file.txt

nothing added to commit but untracked files present (use "git add" to track)
PS D:\old\The Gym\git-exercises> git branch
PS D:\old\The Gym\git-exercises> git branch --show-current
master
PS D:\old\The Gym\git-exercises> git branch -m main
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        file.txt

nothing added to commit but untracked files present (use "git add" to track)
PS D:\old\The Gym\git-exercises> git branch
PS D:\old\The Gym\git-exercises> git branch --show-current
master
PS D:\old\The Gym\git-exercises> git branch -m main

```

## Bundle 1
## Exercise 2

```bash 
PS D:\old\The Gym\git-exercises> new-Item -ItemType File -Path home.html

    Directory: D:\old\The Gym\git-exercises

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a---           8/19/2025  3:49 PM              0 home.html

PS D:\old\The Gym\git-exercises> git add home.html
PS D:\old\The Gym\git-exercises> new-Item -ItemType File -Path about.html

    Directory: D:\old\The Gym\git-exercises

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a---           8/19/2025  4:00 PM              0 about.html

PS D:\old\The Gym\git-exercises> git add about.html
PS D:\old\The Gym\git-exercises> new-Item -ItemType File -Path team.html 

    Directory: D:\old\The Gym\git-exercises

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a---           8/19/2025  4:01 PM              0 team.html

PS D:\old\The Gym\git-exercises> 
PS D:\old\The Gym\git-exercises> git add team.html 
PS D:\old\The Gym\git-exercises> git add .
PS D:\old\The Gym\git-exercises> git stash list
PS D:\old\The Gym\git-exercises> git status    
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
        new file:   about.html
        new file:   home.html
        new file:   team.html
PS D:\old\The Gym\git-exercises> git stash
Saved working directory and index state WIP on dev: b5cfaff additional commands i have used
PS D:\old\The Gym\git-exercises> git list 
PS D:\old\The Gym\git-exercises> git stash list
stash@{0}: WIP on dev: b5cfaff additional commands i have used
PS D:\old\The Gym\git-exercises> 
```