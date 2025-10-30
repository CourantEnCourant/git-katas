# Git Kata: 3-Way Merge

## Setup

1. Run `source setup.sh` (or `.\setup.ps1` in PowerShell)

## The task

You again live in your own branch, this time we will be doing a bit of juggling with branches, to show how lightweight branches are in git.

1. Create a branch called greeting and switch to it
- Done
2. Edit the greeting.txt to contain your favorite greeting
- Done
3. Add greeting.txt files to the staging area
- Done
4. Commit
- Done
5. Switch back to the master branch
- Done
6. Create a file README.md with information about this repository
- Done
7. Add the README.md file to staging area and make the commit
- Done
8. What is the output of `git log --oneline --graph --all`?
- One "greeting" branch there is the favorite greeting and "master" branch there is README update
9. Diff the branches
- Done
10. Merge the greeting branch into master
- Done
11. What is the output of `git log --oneline --graph --all` now? Observe the extra merge commit created with the message "Merge branch 'greeting'".
- A very cool graph where the "greeting" branch got merged into "master"
- BTW I can delete the "greeting" branch and the log stays the same

## Useful commands

- `git branch`
- `git branch <branch-name>`
- `git branch -d <branch-name>`
- `git switch <branch-name>`
- `git switch -c <branch-name>`
- `git branch -v`
- `git add`
- `git commit`
- `git commit -m`
- `git merge <branch-name>`
- `git diff <branchA> <branchB>`
- `git log --oneline --graph --all`
