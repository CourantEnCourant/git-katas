# Git Kata: Basic Staging

This kata will examine the staging area of git.

In git we are working with three different areas:

* The working directory where you are making your changes
* The staging area where all changes you have added through `git add` will stay
* The repository where every commit ends up, making your history. To put your staged changes in here you issue the `git commit` command.

A file can have changes both in the working directory and staging area at the same time.
These changes do not have to be the same.

We will also work with `git restore` to restore the staged changes of a file, and `git checkout` to return a file to a previous state.

## Setup

1. Run `source setup.sh` (or `.\setup.ps1` in PowerShell)

## The task

You live in your own repository. There is a file called `file.txt`.

1. What's the content of `file.txt`? 
- 1
2. Overwrite the content in `file.txt`: `echo 2 > file.txt` to change the state of your file in the working directory (or `sc file.txt '2'` in PowerShell)
- Done
3. What does `git diff` tell you?
- -1 +2 for file.txt
4. What does `git diff --staged` tell you? why is this blank?
- Nothing. Cuz we haven't staged it yet
5. Run `git add file.txt` to stage your changes from the working directory.
- Done
6. What does `git diff` tell you?
- Nothing. Cuz "git diff" compares what the current dir with the staged dir
7. What does `git diff --staged` tell you?
- -1 +2
8. Overwrite the content in `file.txt`: `echo 3 > file.txt` to change the state of your file in the working directory (or `sc file.txt '3'` in PowerShell).
- Done
9. What does `git diff` tell you?
- -2 +3
10. What does `git diff --staged` tell you?
-1 +2
11. Explain what is happening
- "git diff" compares current dir with the staged dir. "git diff --staged" compares the staged area with the last commit
12. Run `git status` and observe that `file.txt` are present twice in the output.
- Done
13. Run `git restore --staged file.txt` to unstage the change
- Done
14. What does `git status` tell you now?
- Changes on "file.txt" but nothing staged
15. Stage the change and make a commit
- Done
16. What does the log look like?
- There is a new commit?
17. Overwrite the content in `file.txt`: `echo 4 > file.txt` (or `sc file.txt '4'` in PowerShell)
- Done
18. What is the content of `file.txt`?
- 4
19. What does `git status` tell us?
- "file.txt" got changed
20. Run `git restore file.txt`
- Done
21. What is the content of `file.txt`?
- 3
22. What does `git status` tell us?
- Nothing to commit

## Useful commands

- `git add`
- `git commit`
- `git commit -m "My lazy short commit message"`
- `git log`
- `git log -n 5`
- `git log --oneline`
- `git log --oneline --graph`
- `git restore --staged`

## Aliases

You can set up aliases as such:
`git config --global alias.lol 'log --oneline --graph --all'`
This might be useful to you.
