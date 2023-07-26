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