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

$ git switch -c dev
Switched to a new branch 'dev'

$ git switch -c test
Switched to a new branch 'test'

$ git switch dev
Switched to branch 'dev'
M       README.md

$ git branch -d test
Deleted branch test (was 6eef24c).

```