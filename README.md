# Git Exercises

## Bundle 1

### Exercise 1

```
origin  https://github.com/riyoneri/gym-git-exercise-solutions.git (fetch)
origin  https://github.com/riyoneri/gym-git-exercise-solutions.git (push)

$ git add index.html 

$ git commit -m "Initial commit"
[main (root-commit) aacc023] Initial commit
 1 file changed, 11 insertions(+)
 create mode 100644 index.html

 $ git switch -c dev
Switched to a new branch 'dev'

git switch -c test
Switched to a new branch 'test'

$ git switch dev 
Switched to branch 'dev'

$ git branch
* dev
  main
  test

$ git branch -d test 
Deleted branch test (was 34da32a).
```

## Bunde 1

### Exercise 2

```
$ git stash
No local changes to save

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git stash list
stash@{0}: WIP on main: f5641e6 Add bundle1-exercise1 to readme
stash@{1}: WIP on main: f5641e6 Add bundle1-exercise1 to readme

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git stash pop stash@{1
error: stash@{1 is not a valid reference

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git stash pop stash@{1}
Already up to date.
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{1} (df6437d658b971802334d6fd620f021e684c2245)

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git stash pop stash@{0} 
Already up to date.
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        team.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{0} (4e18371aa4d2c66aecd0f65ba70fddf3fead3d16)

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git stash about.html
fatal: subcommand wasn't specified; 'push' can't be assumed due to unexpected token 'about.html'

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git stash push about.html
error: pathspec ':(,prefix:0)about.html' did not match any file(s) known to git
Did you forget to 'git add'?

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git stash push -m "stash about.html" about.html
error: pathspec ':(,prefix:0)about.html' did not match any file(s) known to git
Did you forget to 'git add'?

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git stash push -m "stash about.html" about.html -u
Saved working directory and index state On main: stash about.html

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git stash push -m "stash team.html" team.html -u
Saved working directory and index state On main: stash team.html

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git stash list
stash@{0}: On main: stash team.html
stash@{1}: On main: stash about.html

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git stash pop stash@{0}
Already up to date.
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{0} (a6d8ac193c9b37b5f94674f3ab2591425f5d958b)

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git reset --help

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git reset

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git reset 
dev           HEAD          main          ORIG_HEAD     origin/main

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git reset
dev           HEAD          main          ORIG_HEAD     origin/main

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git reset
dev           HEAD          main          ORIG_HEAD     origin/main

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git reset main 

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git log --oneline 
edc7e9a (HEAD -> main, origin/main) stash and stash pop home.html
f5641e6 (dev) Add bundle1-exercise1 to readme
34da32a Add Readme.md
aacc023 Initial commit

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git log
commit edc7e9a2f98983159984cf2bb78eb87f4b4772a9 (HEAD -> main, origin/main)
Author: Lionel Kaneza <lionkaneza@gmail.com>
Date:   Wed Jul 26 11:14:27 2023 +0200

    stash and stash pop home.html

commit f5641e6394e7f39d66717351e8d9e6772bf792dd (dev)
Author: Lionel Kaneza <lionkaneza@gmail.com>
Date:   Wed Jul 26 10:45:41 2023 +0200

    Add bundle1-exercise1 to readme

commit 34da32afe488c5b90f0db24f949d3f6284221113
Author: Lionel Kaneza <lionkaneza@gmail.com>
Date:   Wed Jul 26 10:23:33 2023 +0200

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git log -h
usage: git log [<options>] [<revision-range>] [[--] <path>...]
   or: git show [<options>] <object>...

    -q, --quiet           suppress diff output
    --source              show source
    --use-mailmap         use mail map file
    --mailmap             alias of --use-mailmap
    --clear-decorations   clear all previously-defined decoration filters
    --decorate-refs <pattern>
                          only decorate refs that match <pattern>
    --decorate-refs-exclude <pattern>
                          do not decorate refs that match <pattern>
    --decorate[=...]      decorate options
    -L <range:file>       trace the evolution of line range <start>,<end> or function :<funcname> in <file>


RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git log --oneline 
edc7e9a (HEAD -> main, origin/main) stash and stash pop home.html
f5641e6 (dev) Add bundle1-exercise1 to readme
34da32a Add Readme.md
aacc023 Initial commit

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git reset edc7e9a

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git log --oneline 
edc7e9a (HEAD -> main, origin/main) stash and stash pop home.html
f5641e6 (dev) Add bundle1-exercise1 to readme
34da32a Add Readme.md
aacc023 Initial commit

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git reset edc7e9a

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git log --oneline 
edc7e9a (HEAD -> main, origin/main) stash and stash pop home.html
f5641e6 (dev) Add bundle1-exercise1 to readme
34da32a Add Readme.md
aacc023 Initial commit

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git reset 
dev           HEAD          main          ORIG_HEAD     origin/main

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git reset
dev           HEAD          main          ORIG_HEAD     origin/main

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git reset 34da32a
Unstaged changes after reset:
M       README.md

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git add .

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$
```

## Bundle 2

### Execercise 1

```
RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git switch -c ft/bundle-2
Switched to a new branch 'ft/bundle-2'

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/bundle-2)
$ git add .

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/bundle-2)
$ git commit -m "add services.html"
[ft/bundle-2 c74b051] add services.html
 1 file changed, 11 insertions(+)
 create mode 100644 services.html

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/bundle-2)
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/bundle-2)
$ git push origin
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/bundle-2)
$ git push origin ft/bundle-2 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 440 bytes | 146.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/riyoneri/gym-git-exercise-solutions/pull/new/ft/bundle-2
remote:
To https://github.com/riyoneri/gym-git-exercise-solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
```


## Bundle 2

### Execercise 2

```
RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git branch -c ft/service-redesign

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git add .

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git commit -m "add services"
[main faeb3cb] add services
 1 file changed, 2 insertions(+)

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git push
To https://github.com/riyoneri/gym-git-exercise-solutions.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/riyoneri/gym-git-exercise-solutions.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git branch
  dev
  ft/bundle-2
  ft/service-redesign
* main

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/main'.

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/service-redesign)
$ git merge main 
Updating caf9403..faeb3cb
Fast-forward
 services.html | 2 ++
 1 file changed, 2 insertions(+)

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/service-redesign)
$ git push origin ft/service-redesign 
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 8 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 1.36 KiB | 279.00 KiB/s, done.
Total 7 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote: 
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/riyoneri/gym-git-exercise-solutions/pull/new/ft/service-redesign
remote:
To https://github.com/riyoneri/gym-git-exercise-solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

 $ git checkout main 
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git add .

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git commit -m "add services"
[main 7e960f0] add services
 1 file changed, 2 insertions(+), 2 deletions(-)

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git push
To https://github.com/riyoneri/gym-git-exercise-solutions.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/riyoneri/gym-git-exercise-solutions.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git pull
remote: Enumerating objects: 11, done.
remote: Counting objects: 100% (11/11), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 7 (delta 2), reused 2 (delta 1), pack-reused 0
Unpacking objects: 100% (7/7), 2.75 KiB | 13.00 KiB/s, done.
From https://github.com/riyoneri/gym-git-exercise-solutions
   caf9403..a77c07e  main       -> origin/main
Merge made by the 'ort' strategy.

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git push
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 482 bytes | 482.00 KiB/s, done.
Total 4 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
To https://github.com/riyoneri/gym-git-exercise-solutions.git
   a77c07e..878991f  main -> main

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git add .

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git commit -m "add terminal output to readme"
[main 944c5e6] add terminal output to readme
 1 file changed, 57 insertions(+)

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 1.04 KiB | 355.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/riyoneri/gym-git-exercise-solutions.git
   878991f..944c5e6  main -> main

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git checkout ft/service-redesign 
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/service-redesign)
$ git diff main
diff --git a/README.md b/README.md
index 566495a..c8f8077 100644
--- a/README.md
+++ b/README.md
@@ -285,24 +285,22 @@ To https://github.com/riyoneri/gym-git-exercise-solutions.git
  * [new branch]      ft/bundle-2 -> ft/bundle-2


RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/service-redesign)
$ git merge main
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/service-redesign|MERGING)
$ git add .

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/service-redesign|MERGING)
$ git commit -m "resolve ft/service-redesign merging conflicts"
[ft/service-redesign cd0442d] resolve ft/service-redesign merging conflicts

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/service-redesign)
$
```


## Bundle 3

### Exercise 1

```
RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git switch -c ft/team-page
Switched to a new branch 'ft/team-page'

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/team-page)
$ git add .

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/team-page)
$ git commit -m "add somechanges to team.html"
[ft/team-page 989fe3f] add somechanges to team.html
 1 file changed, 1 insertion(+), 1 deletion(-)

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/team-page)
$ git push origin ft/team-page 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 328 bytes | 164.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/riyoneri/gym-git-exercise-solutions/pull/new/ft/team-page
remote:
To https://github.com/riyoneri/gym-git-exercise-solutions.git
 * [new branch]      ft/team-page -> ft/team-page

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git switch -c ft/contact-page
Switched to a new branch 'ft/contact-page'

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/contact-page)
$ git switch ft/team-page 
Switched to branch 'ft/team-page'

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/team-page)
$ git log
commit 989fe3f606bd79ae8220555857b7dcecef40ed31 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Lionel Kaneza <lionkaneza@gmail.com>
Date:   Mon Jul 31 17:43:16 2023 +0200

    add somechanges to team.html

commit 91d93a8c0b3cf298e96984f1183e2c53b1cc2aaa (origin/main, main, ft/contact-page)
Merge: 0029316 d5a6b9a
Author: Lionel Kaneza <113932119+riyoneri@users.noreply.github.com>
Date:   Mon Jul 31 18:39:05 2023 +0300

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/team-page)
$ git log --oneline 
989fe3f (HEAD -> ft/team-page, origin/ft/team-page) add somechanges to team.html
91d93a8 (origin/main, main, ft/contact-page) Merge pull request #5 from riyoneri/ft/service-redesign
d5a6b9a (origin/ft/service-redesign, ft/service-redesign) correct erros in readme
0029316 Merge pull request #4 from riyoneri/ft/service-redesign
0e2b161 add terminal output to readme Bundle2 exercise2
cd0442d resolve ft/service-redesign merging conflicts
944c5e6 add terminal output to readme
878991f Merge branch 'main' of https://github.com/riyoneri/gym-git-exercise-solutions
7e960f0 add services
d2b0ec6 add bundle2 exercise2 terminal output to readme
faeb3cb add services
a77c07e Merge pull request #3 from riyoneri/revert-2-ft/service-redesign
07a27f9 Revert "add more services to services.html"
85ad50d Merge pull request #2 from riyoneri/ft/service-redesign
797a9a2 Merge branch 'main' into ft/service-redesign
caf9403 add main services to services.html
e4a427e add more services to services.html
a7964f0 Merge pull request #1 from riyoneri/ft/bundle-2
105671e (origin/ft/bundle-2, ft/bundle-2) add terminal output for bundle2#exercise1
c74b051 add services.html
50f63fe resolving error
098e1dd add terminal for bundle1-exercise 2
edc7e9a stash and stash pop home.html
f5641e6 (dev) Add bundle1-exercise1 to readme
34da32a Add Readme.md
aacc023 Initial commit

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/team-page)
$ git checkout ft/contact-page 
Switched to branch 'ft/contact-page'

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/contact-page)
$ git cherry
cherry        cherry-pick

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/contact-page)
$ git cherry
cherry        cherry-pick

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/contact-page)
$ git cherry
cherry        cherry-pick

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/contact-page)
$ git cherry-pick 989fe3f
[ft/contact-page 7e6d314] add somechanges to team.html
 Date: Mon Jul 31 17:43:16 2023 +0200
 1 file changed, 1 insertion(+), 1 deletion(-)

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/contact-page)
$ git log --oneline 
7e6d314 (HEAD -> ft/contact-page) add somechanges to team.html
91d93a8 (origin/main, main) Merge pull request #5 from riyoneri/ft/service-redesign
d5a6b9a (origin/ft/service-redesign, ft/service-redesign) correct erros in readme
0029316 Merge pull request #4 from riyoneri/ft/service-redesign
0e2b161 add terminal output to readme Bundle2 exercise2
cd0442d resolve ft/service-redesign merging conflicts
944c5e6 add terminal output to readme
878991f Merge branch 'main' of https://github.com/riyoneri/gym-git-exercise-solutions
7e960f0 add services
d2b0ec6 add bundle2 exercise2 terminal output to readme

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/contact-page)
$ git add .

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/contact-page)
$ git commit -m "add contact.html"
[ft/contact-page 5591d08] add contact.html
 1 file changed, 11 insertions(+)
 create mode 100644 contact.html

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/contact-page)
$ git push origin ft/contact-page 
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 726 bytes | 242.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/riyoneri/gym-git-exercise-solutions/pull/new/ft/contact-page
remote:
To https://github.com/riyoneri/gym-git-exercise-solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/contact-page)
$ git switch -c ft/faq-page
Switched to a new branch 'ft/faq-page'

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/faq-page)
$ git add .

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/faq-page)
$ git commit -m "add faq.html"
[ft/faq-page c82327c] add faq.html
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/faq-page)
$ git push origin ft/faq-page 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 440 bytes | 220.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/riyoneri/gym-git-exercise-solutions/pull/new/ft/faq-page
remote:
To https://github.com/riyoneri/gym-git-exercise-solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page


RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/faq-page)
$ git revert c82327c33f25fe5371150b0d5fedbd174670ef6a
[ft/faq-page 10057e5] Revert "add faq.html"
 1 file changed, 11 deletions(-)
 delete mode 100644 faq.html
```

## Bundle 3

### Exercise 2

```
RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/faq-page)
$ git switch -c ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/home-page-redesign)
$ git checkout main 
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git commit -m "some changes in main"
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html
        modified:   services.html

no changes added to commit (use "git add" and/or "git commit -a")

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git add .

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git commit -m "some new changes in main"
[main 9d6d192] some new changes in main
 2 files changed, 2 insertions(+), 2 deletions(-)

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git push
To https://github.com/riyoneri/gym-git-exercise-solutions.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/riyoneri/gym-git-exercise-solutions.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git pull
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 1.84 KiB | 23.00 KiB/s, done.
From https://github.com/riyoneri/gym-git-exercise-solutions
   91d93a8..79ac37c  main       -> origin/main
Merge made by the 'ort' strategy.
 README.md    | 189 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 contact.html |  11 ++++
 2 files changed, 199 insertions(+), 1 deletion(-)
 create mode 100644 contact.html

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git push
Enumerating objects: 12, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 8 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 732 bytes | 732.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), completed with 3 local objects.
To https://github.com/riyoneri/gym-git-exercise-solutions.git
   79ac37c..ff55d85  main -> main

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (main)
$ git switch ft/home-page-redesign 
Switched to branch 'ft/home-page-redesign'

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/home-page-redesign)
$ git rebase --h
error: unknown option `h'
usage: git rebase [-i] [options] [--exec <cmd>] [--onto <newbase> | --keep-base] [<upstream> [<branch>]]
   or: git rebase [-i] [options] [--exec <cmd>] [--onto <newbase>] --root [<branch>]
   or: git rebase --continue | --abort | --skip | --edit-todo

    --onto <revision>     rebase onto given branch instead of upstream
    --keep-base           use the merge-base of upstream and branch as the current base
    --no-verify           allow pre-rebase hook to run
    -q, --quiet           be quiet. implies --no-stat
    -v, --verbose         display a diffstat of what changed upstream
    -n, --no-stat         do not show diffstat of what changed upstream
    --signoff             add a Signed-off-by trailer to each commit
    --committer-date-is-author-date
                          make committer date match author date
    --reset-author-date   ignore author date and use current date
    -C <n>                passed to 'git apply'
    --ignore-whitespace   ignore changes in whitespace
    --whitespace <action>
                          passed to 'git apply'
    -f, --force-rebase    cherry-pick all commits, even if unchanged
    --no-ff               cherry-pick all commits, even if unchanged
    --continue            continue
    --skip                skip current patch and continue
    --abort               abort and check out the original branch
    --quit                abort but keep HEAD where it is
    --edit-todo           edit the todo list during an interactive rebase
    --show-current-patch  show the patch file being applied or merged
    --apply               use apply strategies to rebase
    -m, --merge           use merging strategies to rebase
    -i, --interactive     let the user edit the list of commits to rebase
    --rerere-autoupdate   update the index with reused conflict resolution if possible
    --empty <{drop,keep,ask}>
                          how to handle commits that become empty
    --autosquash          move commits that begin with squash!/fixup! under -i
    --update-refs         update branches that point to commits that are being rebased
    -S, --gpg-sign[=<key-id>]
                          GPG-sign commits
    --autostash           automatically stash/stash pop before and after
    -x, --exec <exec>     add exec lines after each commit of the editable list
    -r, --rebase-merges[=<mode>]
                          try to rebase merges instead of skipping them
    --fork-point          use 'merge-base --fork-point' to refine upstream
    -s, --strategy <strategy>
                          use the given merge strategy
    -X, --strategy-option <option>
                          pass the argument through to the merge strategy
    --root                rebase all reachable commits up to the root(s)
    --reschedule-failed-exec
                          automatically re-schedule any `exec` that fails
    --reapply-cherry-picks
                          apply all changes, even those already present upstream


RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/home-page-redesign)
$ git rebase --h
error: unknown option `h'
usage: git rebase [-i] [options] [--exec <cmd>] [--onto <newbase> | --keep-base] [<upstream> [<branch>]]
   or: git rebase [-i] [options] [--exec <cmd>] [--onto <newbase>] --root [<branch>]
   or: git rebase --continue | --abort | --skip | --edit-todo

    --onto <revision>     rebase onto given branch instead of upstream
    --keep-base           use the merge-base of upstream and branch as the current base
    --no-verify           allow pre-rebase hook to run
    -q, --quiet           be quiet. implies --no-stat
    -v, --verbose         display a diffstat of what changed upstream
    -n, --no-stat         do not show diffstat of what changed upstream
    --signoff             add a Signed-off-by trailer to each commit
    --committer-date-is-author-date
                          make committer date match author date
    --reset-author-date   ignore author date and use current date
    -C <n>                passed to 'git apply'
    --ignore-whitespace   ignore changes in whitespace
    --whitespace <action>
                          passed to 'git apply'
    -f, --force-rebase    cherry-pick all commits, even if unchanged
    --no-ff               cherry-pick all commits, even if unchanged
    --continue            continue
    --skip                skip current patch and continue
    --abort               abort and check out the original branch
    --quit                abort but keep HEAD where it is
    --edit-todo           edit the todo list during an interactive rebase
    --show-current-patch  show the patch file being applied or merged
    --apply               use apply strategies to rebase
    -m, --merge           use merging strategies to rebase
    -i, --interactive     let the user edit the list of commits to rebase
    --rerere-autoupdate   update the index with reused conflict resolution if possible
    --empty <{drop,keep,ask}>
                          how to handle commits that become empty
    --autosquash          move commits that begin with squash!/fixup! under -i
    --update-refs         update branches that point to commits that are being rebased
    -S, --gpg-sign[=<key-id>]
                          GPG-sign commits
    --autostash           automatically stash/stash pop before and after
    -x, --exec <exec>     add exec lines after each commit of the editable list
    -r, --rebase-merges[=<mode>]
                          try to rebase merges instead of skipping them
    --fork-point          use 'merge-base --fork-point' to refine upstream
    -s, --strategy <strategy>
                          use the given merge strategy
    -X, --strategy-option <option>
                          pass the argument through to the merge strategy
    --root                rebase all reachable commits up to the root(s)
    --reschedule-failed-exec
                          automatically re-schedule any `exec` that fails
    --reapply-cherry-picks
                          apply all changes, even those already present upstream


RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/home-page-redesign)
$ git rebase -h
usage: git rebase [-i] [options] [--exec <cmd>] [--onto <newbase> | --keep-base] [<upstream> [<branch>]]
   or: git rebase [-i] [options] [--exec <cmd>] [--onto <newbase>] --root [<branch>]
   or: git rebase --continue | --abort | --skip | --edit-todo

    --onto <revision>     rebase onto given branch instead of upstream
    --keep-base           use the merge-base of upstream and branch as the current base
    --no-verify           allow pre-rebase hook to run
    -q, --quiet           be quiet. implies --no-stat
    -v, --verbose         display a diffstat of what changed upstream
    -n, --no-stat         do not show diffstat of what changed upstream
    --signoff             add a Signed-off-by trailer to each commit
    --committer-date-is-author-date
                          make committer date match author date
    --reset-author-date   ignore author date and use current date
    -C <n>                passed to 'git apply'
    --ignore-whitespace   ignore changes in whitespace
    --whitespace <action>
                          passed to 'git apply'
    -f, --force-rebase    cherry-pick all commits, even if unchanged
    --no-ff               cherry-pick all commits, even if unchanged
    --continue            continue
    --skip                skip current patch and continue
    --abort               abort and check out the original branch
    --quit                abort but keep HEAD where it is
    --edit-todo           edit the todo list during an interactive rebase
    --show-current-patch  show the patch file being applied or merged
    --apply               use apply strategies to rebase
    -m, --merge           use merging strategies to rebase
    -i, --interactive     let the user edit the list of commits to rebase
    --rerere-autoupdate   update the index with reused conflict resolution if possible
    --empty <{drop,keep,ask}>
                          how to handle commits that become empty
    --autosquash          move commits that begin with squash!/fixup! under -i
    --update-refs         update branches that point to commits that are being rebased
    -S, --gpg-sign[=<key-id>]
                          GPG-sign commits
    --autostash           automatically stash/stash pop before and after
    -x, --exec <exec>     add exec lines after each commit of the editable list
    -r, --rebase-merges[=<mode>]
                          try to rebase merges instead of skipping them
    --fork-point          use 'merge-base --fork-point' to refine upstream
    -s, --strategy <strategy>
                          use the given merge strategy
    -X, --strategy-option <option>
                          pass the argument through to the merge strategy
    --root                rebase all reachable commits up to the root(s)
    --reschedule-failed-exec
                          automatically re-schedule any `exec` that fails
    --reapply-cherry-picks
                          apply all changes, even those already present upstream


RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/home-page-redesign)
$ git rebase --help

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/home-page-redesign)
$ git add .

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/home-page-redesign)
$ git commit -m "add some changes in indes[ft/home-page-redesign]"
[ft/home-page-redesign 02ecdc2] add some changes in indes[ft/home-page-redesign]
 1 file changed, 1 insertion(+), 1 deletion(-)

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/home-page-redesign)
$ git push origin ft/home-page-redesign 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 364 bytes | 364.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/riyoneri/gym-git-exercise-solutions/pull/new/ft/home-page-redesign
remote:
To https://github.com/riyoneri/gym-git-exercise-solutions.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign

RIYO@DESKTOP-DETFET6 MINGW64 /d/Codes/009 - Studies/001 - The-Gym/001 - git/002 - gym-git-exercise-solutions (ft/home-page-redesign)
$
```

