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
 ```

+
 ## Bundle 2

-### Execercise 2 main

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