# Git and Github 

## Task 1 
Demonstrate minimum 15 basic Git command with explanation and screenshot.

1. git add - Add file contents to the index
2. git status - Show the working tree status
```
% git add .
% git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   GitDocker/assignment-1.md
```
3. git log - Show commit logs
```
% git log
commit b28828e48f529a805186d7f6ea3ad68a73ba7040 (HEAD -> main, origin/main)
Author: Batbayar Bold <bold.bb@gmail.com>
Date:   Sat Oct 15 13:32:45 2022 +0200

    third commit
```
4. git init - Create an empty Git repository or reinitialize an existing one
```
% git init
Reinitialized existing Git repository in /Users/batbayarbold/ds-projects/.git/ 
```
5. git commit - Record changes to the repository
```
% git commit -m "first 5 git commands"
[main 5af4b00] first 5 git commands
 1 file changed, 39 insertions(+), 1 deletion(-)
```
6. git push - Update remote refs along with associated objects
```
% git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 916 bytes | 916.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/batbayar-bold/ds-projects.git
   c567356..5af4b00  main -> main
```
7. git branch - List, create, or delete branches
8. git switch - Switch branches
```
% git branch 
* main
% git branch feature
% git switch feature
Switched to branch 'feature'
```
9. git restore - Restore working tree files
10. git rm - Remove files from the working tree and from the index
11. git diff - Show changes between commits, commit and working tree, etc
12. git grep - Print lines matching a pattern
13. git rebase - Reapply commits on top of another base tip
14. git reset - Reset current HEAD to the specified state
15. git pull - Fetch from and integrate with another repository or a local branch


## Task 2 
Consider that your want to start an open-source project in your organization. Perform all the standard operation to create a repository with minimal permision for all the users. It should contain.
1. Proper open source structure 
2. Proper Readme
3. Add 2 collaborator 
4. Host GitHub Pages using settings (Designed to host your personal, organization, or project pages from a GitHub repository)

```
https://batbayar-bold.github.io/open-source-project/
```

## Task 3 
1. Create a Issue in your github repository.
2. Raise a pull request.
3. Merge A pull request.
4. Reject a pull request with proper comments.
5. Add a Dependabot alerts in your github.(for above cases)
6. Stash changes
7. Create a release your package
8. Setup a Projects Board for your project.
```
https://batbayar-bold.github.io/open-source-project/
```