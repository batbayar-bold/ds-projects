# Git and Github 

### Task 1 
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
% git commit -m "first 4 git commands"
[main c567356] first 4 git commands
 1 file changed, 3 insertions(+)
 create mode 100644 GitDocker/assignment-1.md
```



