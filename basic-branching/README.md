# Git Kata: Basic Branching

## Setup

1. Run `source setup.sh` (or `.\setup.ps1` in PowerShell)

## The task

You again live in your own branch, this time we will be doing a bit of juggling with branches, to show how lightweight branches are in git.
Hint: `git switch` will make you switch from one branch to another.

1. Use `git branch` to see the two branches that are relevant for this exercise
- Done
2. What branch are you on?
- "master"
3. Use `git branch mybranch` to create a new branch called _mybranch_
- Done
4. Use `git branch` again to see the new branch created.
- Done
5. Use `git switch mybranch` to switch to your new branch.
- Done
6. How does the output from `git status` change when you switch between the _master_ and the new branch that you have created?
- Nothing to commit
7. How does the workspace change when you change between the two branches?
- Nothing changed
8. Make sure you are on your _mybranch_ branch before you continue.
- Done
9. Create a file called `file1.txt` with your name.
- Done
10. `Add` the file and `commit` with this change.
- Done
11. Use `git log --oneline --graph` to see your branch pointing to the new commit.
- Done
12. Switch back to the branch called _master_.
- Done
13. Use `git log --oneline --graph` and notice how the commit you made on the _mybranch_ branch is missing on the _master_ branch.
- Done
14. Make a new file called `file2.txt` and commit that file.
- Done
15. Use `git log --oneline --graph --all` to see your branch pointing to the new commit, and that the two branches now have different commits on them.
- Done
16. Switch to your branch _mybranch_.
- Done
17. What happened to your working directory? Can you see your `file2.txt`?
- No
18. Use `git diff mybranch master` to see the difference between the two branches.
- Wow I didn't know that "git diff" can compare different branches. There is also a from-to relation.

## Useful commands

- `git switch`
- `git switch -c`
- `git log --oneline --graph`
- `git branch`
- `git diff`
