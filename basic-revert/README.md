# Git Kata: Basic revert
## Setup:

1. Run `source setup.sh` (or `.\setup.ps1` in PowerShell)

## The task

In this task a few changes snuck in, that we'd like to get out. Our history is public, so we can't just change it. Rather we need to use revert to remove the unwanted changes in a safe way.

1. Use `git log --oneline` to look at the history
- Done
2.  Use `cat` to view the content of `greeting.txt`
- Done
3.  Use `git revert` on the newest commit, to remove the changes the last commit added
- "git revert HEAD~1", resulted in conflict, and solved with mergetool
4.  Use `git log --oneline` to view the history
- Done
5.  Did the revert command add or remove a commit?
- It added a commit
6.  Use `cat` to view the content of `greeting.txt`
- It's the original content
7.  Use `ls` to see the content of the workspace
- Two files present, `credentials.txt` and `greeting.txt`
8.  Use `git log --oneline` to find the sha of the commit adding credentials to the repository
- Surprise to see that with oneline the sha is only 7-digit long. Will it work?
9.  Use `git revert` to revert the commit that added the credentials
- The shortened commit SHA actually worked!
10. Use `git log --oneline` to view the history
- Just says it reverted the targeted commit
11. Use `ls` to see the content of the workspace
- `credentials.txt` is gone
12. How many commits were added or changed by the last revert?
- One
13. Use `git show` with the sha of the commit you reverted to see that the credentials file is still in the history
- Interesting to see that the `/dev/null` is used to indicate the file creation and deletion
14. As you have now reverted the credentials file, so it is removed from your working directory, is it also removed from git?
- Of course not. "You can checkout at anytime you like, but you may never leave" -- Hotel California

## Useful commands
- `git revert <ref>`
- `git log --oneline`
- `git show <ref>`
