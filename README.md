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


## Bundle 2
## Exercise 2

```bash
PS D:\old\The Gym\git-exercises> git pull
Already up to date.
PS D:\old\The Gym\git-exercises> git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'
PS D:\old\The Gym\git-exercises> echo "<h1>This is a service page</h1>"
<h1>This is a service page</h1>
PS D:\old\The Gym\git-exercises> echo "<h1>This is a service page</h1>" >> service.html
PS D:\old\The Gym\git-exercises> git add service.html
PS D:\old\The Gym\git-exercises> git commit -m " I created service page"
[ft/service-redesign 392b0c2]  I created service page
 1 file changed, 1 insertion(+)
 create mode 100644 service.html
 PS D:\old\The Gym\git-exercises> git push origin ft/service-redesign
>>
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 302 bytes | 302.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/ishluc12/Git-Exercise/pull/new/ft/service-redesign
remote:
To https://github.com/ishluc12/Git-Exercise.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
PS D:\old\The Gym\git-exercises> git branch
  dev
  ft/bundle-2
  ft/service-redesign
* main
PS D:\old\The Gym\git-exercises> git add service.html
PS D:\old\The Gym\git-exercises> git commit  -m "new changes to service name"
[main b37e8ce] new changes to service name
 1 file changed, 1 insertion(+)
 create mode 100644 service.html
PS D:\old\The Gym\git-exercises> git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 267 bytes | 267.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/ishluc12/Git-Exercise.git
   d19cb76..b37e8ce  main -> main
PS D:\old\The Gym\git-exercises> git add --all
PS D:\old\The Gym\git-exercises> git commit -m "I added changes to the service page"
[main 6c25d62] I added changes to the service page
 3 files changed, 15 insertions(+), 3 deletions(-)
 delete mode 100644 services.html
PS D:\old\The Gym\git-exercises> git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 514 bytes | 257.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ishluc12/Git-Exercise.git
   b37e8ce..6c25d62  main -> main
PS D:\old\The Gym\git-exercises> git checkout ft/service-redesign   
>> 
Switched to branch 'ft/service-redesign'
PS D:\old\The Gym\git-exercises> git merge main
Auto-merging service.html
CONFLICT (add/add): Merge conflict in service.html
Automatic merge failed; fix conflicts and then commit the result.
PS D:\old\The Gym\git-exercises> git diff main       
PS D:\old\The Gym\git-exercises> git diff main..ft/service-redesign
diff --git a/README.md b/README.md
index fdeff38..0187e37 100644
--- a/README.md
+++ b/README.md
@@ -157,5 +157,4 @@ To https://github.com/ishluc12/Git-Exercise.git
  * [new branch]      ft/bundle-2 -> ft/bundle-2
 branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
 PS D:\old\The Gym\git-exercises>
-```
-
+```
\ No newline at end of file
diff --git a/service.html b/service.html
index 04ec959..125bea5 100644
--- a/service.html
+++ b/service.html
@@ -1,13 +1 @@
-
-<!DOCTYPE html>
-<html lang="en">
-<head>
-    <meta charset="UTF-8">
-    <meta name="viewport" content="width=device-width, initial-scale=1.0">
PS D:\old\The Gym\git-exercises> git add service.html
PS D:\old\The Gym\git-exercises> git fetch origin    
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (1/1), 885 bytes | 221.00 KiB/s, done.
From https://github.com/ishluc12/Git-Exercise
   392b0c2..4b144e9  ft/service-redesign -> origin/ft/service-redesign
PS D:\old\The Gym\git-exercises> git merge origin/main
fatal: You have not concluded your merge (MERGE_HEAD exists).
Please, commit your changes before you merge.
PS D:\old\The Gym\git-exercises> git add service.html 
PS D:\old\The Gym\git-exercises> git commit -m "I resolved the conflicts in the branch"
[ft/service-redesign 9fe58ee] I resolved the conflicts in the branch
PS D:\old\The Gym\git-exercises> git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS D:\old\The Gym\git-exercises> git push --set-upstream origin ft/service-redesign
To https://github.com/ishluc12/Git-Exercise.git
 ! [rejected]        ft/service-redesign -> ft/service-redesign (non-fast-forward)
error: failed to push some refs to 'https://github.com/ishluc12/Git-Exercise.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
PS D:\old\The Gym\git-exercises> git fetch origin     
PS D:\old\The Gym\git-exercises> git merge origin/ft/service-redesign
>>
hint: Waiting for your editor to close the file... code --wait: line 1: code: command not found
error: there was a problem with the editor 'code --wait'
Not committing merge; use 'git commit' to complete the merge.
PS D:\old\The Gym\git-exercises> git commit -m "Merge remote-tracking branch 'origin/ft/service-redesign' into ft/service-redesign"
>>
[ft/service-redesign c36e537] Merge remote-tracking branch 'origin/ft/service-redesign' into ft/service-redesign
PS D:\old\The Gym\git-exercises> git merge origin/ft/service-redesign
>>
Already up to date.
PS D:\old\The Gym\git-exercises> git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

PS D:\old\The Gym\git-exercises>   git push --set-upstream origin ft/service-redesign
Enumerating objects: 2, done.
Counting objects: 100% (2/2), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 455 bytes | 455.00 KiB/s, done.
Total 2 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/ishluc12/Git-Exercise.git
   4b144e9..c36e537  ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.
PS D:\old\The Gym\git-exercises>
```
