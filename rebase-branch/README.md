# Git Kata: rebase branch

## Setup

1. Run `source setup.sh` (or `.\setup.ps1` in PowerShell)

## The task

You again live in your own branch, this time we will be doing a bit of juggling with branches, to show how lightweight branches are in git.

1. Which branches exist?
- "master" and "uppercase"
2. Look at the log for the master branch
- "add file greeting.txt", "add content to greeting.txt", "add readme"
3. Switch to the uppercase branch
- Done
4. How does the log compare to the log on the master branch?
- For the latest commit, "Change greeting to uppercase"
5. Rebase your uppercase branch with the master (`git rebase master`)
- Done
6. What did just happen? Draw it!
- Bad at drawing. Basically it removes temporarily the latest commit in upper, merges all commits from main, and adds the latest commit on top.
7. Now switch to the master branch
- Done
8. Merge uppercase into master
- Done
9. What does the log look like now?
- Same as "uppercase"

## Useful commands

- `git switch <branch-name>`
- `git rebase <branch-name>`
- `git log --oneline --graph --all`
- `git merge <branch-name>`
