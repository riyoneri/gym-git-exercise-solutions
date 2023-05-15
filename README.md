# Git Exercise

## Bundle 1

### Exercise 1

```bash
$ git init
Initialized empty Git repository in D:/Codes/009 - Studies/001 - Ojemba/001 - git/.git/

$ git branch -M main

$ git add .

$ git commit -m "Initial commit"
[main (root-commit) 9a2cab4] Initial commit
 2 files changed, 2 insertions(+)
 create mode 100644 file1.txt
 create mode 100644 file2.txt

$ git remote add origin https://github.com/riyoneri/gym-git-exercise-solutions.git

$ git push -u origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 2 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 292 bytes | 146.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/riyoneri/gym-git-exercise-solutions.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

```


### Exercise 2

```bash
$ git add home.html

$ git stash
Saved working directory and index state WIP on main: 6eef24c Add README.md file

$ git stash list
stash@{0}: WIP on main: 6eef24c Add README.md file

$ git add about.html

$ git stash
Saved working directory and index state WIP on main: 6eef24c Add README.md file

$ git stash list
stash@{0}: WIP on main: 6eef24c Add README.md file
stash@{1}: WIP on main: 6eef24c Add README.md file

$ git add team.html

$ git stash
Saved working directory and index state WIP on main: 6eef24c Add README.md file

$ git stash list
stash@{0}: WIP on main: 6eef24c Add README.md file
stash@{1}: WIP on main: 6eef24c Add README.md file
stash@{2}: WIP on main: 6eef24c Add README.md file

$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (3d9b6fef9122cd799b886a578d5c640ad49939ff)

$ git stash pop stash@{1}
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

Dropped stash@{1} (e1f011d291cb4e312b7881efb15173658637fe4c)

$ git commit -a -m "Add about.html, home.html"
[main 4d0fa6a] Add about.html, home.html
 3 files changed, 33 insertions(+), 1 deletion(-)
 create mode 100644 about.html
 create mode 100644 home.html

$ git push -u origin dev
Enumerating objects: 11, done.
Counting objects: 100% (11/11), done.
Delta compression using up to 2 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (7/7), 968 bytes | 322.00 KiB/s, done.
Total 7 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
To https://github.com/riyoneri/gym-git-exercise-solutions.git
   ce8a1f5..fef1455  dev -> dev
branch 'dev' set up to track 'origin/dev'.

$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (9971d2bfdeee04ed11d54d460d1aab98acf3431c)

$ git reset --hard
HEAD is now at fef1455 Add about.html, home.html

```

## Bundle 2

### Exercise 1

```bash

$ git switch -c ft/bundle-2
Switched to a new branch 'ft/bundle-2'

$ git add services.html

$ git commit -a -m "Add services.html"
[ft/bundle-2 566a650] Add services.html
 1 file changed, 17 insertions(+)
 create mode 100644 services.html

```