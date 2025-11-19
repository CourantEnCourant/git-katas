# Git Kata: Basic Ignore
We'll work a bit with the `.gitignore` file in this kata.
In this file you can specify both file extensions and folder structures that you do not want Git to track.
You can still `git add` files and folder that are ignored in the `.gitignore` file.

We will also work with `git rm`, which is the Git remove command. `git rm` does just the same as removing a file from your working directory, and then staging that change by issuing a `git add filename` on the file that was just deleted.
Sometimes you add a file by accident that was not meant for Git e.g. binary files, class files etc.

If you want to signal to Git that a file needs to be removed from git, but still want it in your working directory, then use `git rm --cached` to issue a remove command on the staging area, but not in your working directory.


## Setup:

1. Run `source setup.sh` (or `.\setup.ps1` in PowerShell)

## The task

1. Create a file with the name `foo.s`
- Done
2. What is the output of `git status`?
- `file1.txt` and `foo.s` unstaged
3. Create a `.gitignore` file in your working directory containing `*.s`
- Done
4. What is the output of `git status`?
- `file1.txt` and `.gitignore` unstaged
5. Commit the `.gitignore` file
- Done
6. Commit `file1.txt`
- Done
7. Add `txt` files to `.gitignore` by adding a line in the file containing `*.txt`
- Done
8. What does `git status` tell us?
- `.gitignore` unstaged.
9. Change `file1.txt`
- Done
10. What does `git status` tell us? Why was the file tracked even though the `txt` extension is in the ignore file?
- `file1.txt` modified and unstaged. Because the file was already being tracked
11. Make another text file `file2.txt` in the repository, what does `git status` look like now? Why is it not tracked?
- `file2.txt` untracked. Because *.txt in .gitignore and the file is new.
12. Stage the removal of `file1.txt` with the command `git rm --cached`
- Done
13. What does `git status` say?
- `file1.txt` deleted (staged)
14. Create a new file called `file3.txt` and add the line `!file3.txt` to `.gitignore`. (See _note_ below)
- Done
15. What does `git status` say? Can you think of a use-case for keeping track of a file although the extension is ignored?
- Yeah just use ! operator

## Note
If you are using `zsh` instead of `bash`(default on Mac and some Linux') then `echo "!file3.txt" >> .gitignore` will fail because of shell expansion. Either use an editor to modify the file or escape the `!` e.g. `echo "\!file3.txt" >> .gitignore`

## Useful commands
- `git rm`
- `git add`
- `git commit`
- `git commit -m`
- `git rm --cached`


## Aliases
You can set up aliases as such:
`git config --global alias.lol 'log --oneline --graph --all'`
This might be useful to you.
