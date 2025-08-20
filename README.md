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
PS D:\old\The Gym\git-exercises> echo "<h1>home Page</h1>" >>home.html
PS D:\old\The Gym\git-exercises> git stash
No local changes to save
PS D:\old\The Gym\git-exercises> git stash list 
PS D:\old\The Gym\git-exercises> git add home.html
PS D:\old\The Gym\git-exercises> git stash        
Saved working directory and index state WIP on dev: a1ef233 Remove HTML files added by stash
PS D:\old\The Gym\git-exercises> git stash list
stash@{0}: WIP on dev: a1ef233 Remove HTML files added by stash
PS D:\old\The Gym\git-exercises> echo "<h1>about Page</h1>" >>about.html
PS D:\old\The Gym\git-exercises> git add about.html
PS D:\old\The Gym\git-exercises> git stash
Saved working directory and index state WIP on dev: a1ef233 Remove HTML files added by stash
PS D:\old\The Gym\git-exercises> echo "<h1>about Page</h1>" >>team.html
PS D:\old\The Gym\git-exercises> echo "<h1>team Page</h1>" >>team.html
PS D:\old\The Gym\git-exercises> git add team.html
PS D:\old\The Gym\git-exercises> git stash
Saved working directory and index state WIP on dev: a1ef233 Remove HTML files added by stash
PS D:\old\The Gym\git-exercises> git stash list
stash@{0}: WIP on dev: a1ef233 Remove HTML files added by stash
stash@{1}: WIP on dev: a1ef233 Remove HTML files added by stash
stash@{2}: WIP on dev: a1ef233 Remove HTML files added by stash
PS D:\old\The Gym\git-exercises> git stash pop  "stash@{2}"
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Dropped stash@{2} (88ed617b4348e24686f31a5ed071e5671dc8475b)
PS D:\old\The Gym\git-exercises> git stash pop  "stash@{1}"
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (e5c2b9734e347efd4e988df4d9f235af56b35cf1)
PS D:\old\The Gym\git-exercises> git commit -m "add about and home page from stash"
[dev ad7d1f8] add about and home page from stash
 2 files changed, 2 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
PS D:\old\The Gym\git-exercises> git push origin dev
Enumerating objects: 13, done.
Counting objects: 100% (13/13), done.
Delta compression using up to 12 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (11/11), 1.84 KiB | 940.00 KiB/s, done.
Total 11 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), done.
To https://github.com/ishluc12/Git-Exercise.git
   b5cfaff..ad7d1f8  dev -> dev
PS D:\old\The Gym\git-exercises> git stash pop  "stash@{0}"
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (89a86794a265da6e4ef0b2e16dda2a3c901aebaa)
PS D:\old\The Gym\git-exercises> git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html
PS D:\old\The Gym\git-exercises> Remove-Item team.html
```

## Bundle 2
## Exercise 1


```bash

PS D:\old\The Gym\git-exercises> git branch
* dev
  main
PS D:\old\The Gym\git-exercises> git branch ft/bundle-2
PS D:\old\The Gym\git-exercises> git checkout ft/bundle-2
M       README.md
Switched to branch 'ft/bundle-2'
PS D:\old\The Gym\git-exercises> echo "<h1>service page</h1>" >> services.html
PS D:\old\The Gym\git-exercises> git status
On branch ft/bundle-2
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        services.html

no changes added to commit (use "git add" and/or "git commit -a")
PS D:\old\The Gym\git-exercises> git add services.html
PS D:\old\The Gym\git-exercises> git commit -m "adding service page"     
[ft/bundle-2 0af6234] adding service page
 1 file changed, 1 insertion(+)
 create mode 100644 services.html
 
PS D:\old\The Gym\git-exercises> git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 304 bytes | 101.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/ishluc12/Git-Exercise/pull/new/ft/bundle-2
remote:
To https://github.com/ishluc12/Git-Exercise.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
PS D:\old\The Gym\git-exercises> 
```