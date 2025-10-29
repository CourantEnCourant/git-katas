# Git Kata: Fast-forward Merge

## Setup

1. Run `source setup.sh` (or `.\setup.ps1` in PowerShell)

## The task

You again live in your own branch, this time we will be doing a bit of juggling with branches, to show how lightweight branches are in git.

1. Create a (feature)branch called `feature/uppercase` (yes, `feature/uppercase` is a perfectly legal branch name, and a common convention).
- Done. Also this naming convention kinda makes sense
2. Switch to this branch
- Done
3. What is the output of `git status`?
- Nothing to commit
4. Edit the greeting.txt to contain an uppercase greeting
- Done
5. Add `greeting.txt` files to staging area and commit
- Done
6. What is the output of `git branch`?
- There are two branches, "master" and "feature/uppercase"
7. What is the output of `git log --oneline --graph --all`
- There is a new commit on "feature/uppercase" and the "HEAD" is pointed to it

   *Remember: You want to update the master branch so it also has all the changes currently on the feature branch. The command 'git merge [branch name]' takes one branch as argument from which it takes changes. The branch pointed to by HEAD (currently checked out branch) is then updated to also include these changes.*

8. Switch to the `master` branch
- Done
9. Use `cat` to see the contents of the greetings
- Done. It's in lowercase.
10. Diff the branches
- On "master" it's lowercase and "feature/uppercase" it's uppercase
11. Merge the branches
- Done
12. Use `cat` to see the contents of the greetings
- It's now in uppercase
13. Delete the uppercase branch

## Useful commands

- `git branch`
- `git branch <branch-name>`
- `git branch -d <branch-name>`
- `git switch`
- `git branch -v`
- `git add`
- `git commit`
- `git commit -m`
- `git merge <branch>`
- `git diff <branchA> <branchB>`
- `git log --oneline --graph --all`
