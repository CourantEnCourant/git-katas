# Git Kata: Merge Conflict

## Setup:

1. Run `source setup.sh` (or `.\setup.ps1` in PowerShell)

## The task

In this kata git cannot figure out how to merge the content added on `merge-conflict-branch1` with the content on `master`.

Both changes need to be in master when you're done.

1. Use `git merge` to bring the changes from `merge-conflict-branch1` on to `master`.
- Done (failed)
2. What does `git status` now report.
   - Have unmerged paths where I need to fix conflicts
   - "both added: file.txt"
3. Fix the conflict with your favorite editor.
- Done
4. Follow the instructions in `git status` to complete the merge.
- Done
5. What does `git log --oneline --graph` show?
- Merge successful from "merge-conflict-branch1" to "master"

## Relevant commands
- `git merge`
- `git status`
- `git add`
- `git commit`
- `git log --oneline --graph`
