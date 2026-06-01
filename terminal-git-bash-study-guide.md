# Terminal + Git Bash Study Guide

## Git Mastery

### Setup & Config
- `git --version`
  - Confirm Git is installed and see the version number.
- `git config --global user.name "Name"`
  - Set your identity for all commits.
- `git config --global user.email "email"`
  - Set your email for all commits.
- `git config --global core.editor "code --wait"`
  - Use VS Code for commit messages.
- `git config --list`
  - Show all current Git config settings.

### Starting a Repo
- `git init`
  - Start a new repository in the current folder.
- `git clone <url>`
  - Download an existing repo from GitHub to your machine.

### The Core Loop
- `git status`
  - See what files have changed; run this constantly.
- `git add .`
  - Stage all changed files for the next commit.
- `git add <file>`
  - Stage one specific file only.
- `git commit -m "message"`
  - Save a snapshot with a short description.
- `git push origin main`
  - Upload your commits to GitHub.
- `git pull origin main`
  - Download latest changes from GitHub.

### Checking History & Status
- `git log`
  - View the full commit history with author, date, message.
- `git log --oneline`
  - View a compact one-line history.
- `git log --graph main`
  - Visualize branch history.
- `git diff`
  - Show unstaged changes.
- `git diff --staged`
  - Show staged changes ready to commit.
- `git show <commit>`
  - Show what changed in a specific commit.

### Branches
- `git branch`
  - List all branches.
- `git switch -c <name>`
  - Create and switch to a new branch.
- `git switch <name>`
  - Jump to an existing branch.
- `git merge <branch>`
  - Merge another branch into your current branch.
- `git branch -d <name>`
  - Delete a branch safely.

### Remotes
- `git remote -v`
  - Show remote URLs.
- `git remote add origin <url>`
  - Connect a local repo to GitHub.
- `git remote add upstream <url>`
  - Track the original repo after forking.

### Undoing Things
- `git reset <file>`
  - Unstage a file while keeping changes.
- `git restore <file>`
  - Discard changes in a file and revert to the last commit.
- `git commit --amend`
  - Fix the last commit message or add forgotten files.
- `git reset HEAD^`
  - Undo the most recent commit but keep changes in the working tree.
- `git reset --hard`
  - Discard all uncommitted changes completely.
- `git stash`
  - Temporarily save changes without committing.

### Staging Area Tricks
- `git add -p`
  - Pick which parts of a file to stage.
- `git mv old new`
  - Rename or move a file.
- `git rm <file>`
  - Delete a file and stage that deletion.
- `git rm --cached <file>`
  - Stop tracking a file without deleting it from disk.

### Code Archaeology
- `git blame <file>`
  - See who last changed each line.
- `git log <file>`
  - See every commit that touched a file.
- `git log -G "text"`
  - Find every commit that added or removed specific text.

### Referring to Commits
- `HEAD`
  - Your current commit.
- `HEAD^`
  - One commit before the current.
- `HEAD~3`
  - Three commits before the current.
- `<partial-commit-id>`
  - Any partial commit ID from `git log --oneline`.
- `origin/main`
  - The main branch as it exists on GitHub.

## Terminal Mastery (Git Bash / Windows)

### Navigation
- `pwd`
  - Print working directory.
- `cd foldername`
  - Move into a folder.
- `cd ~`
  - Go to your home directory.
- `cd ..`
  - Go up one level.
- `cd ../..`
  - Go up two levels.
- `ls`
  - List files and folders.
- `ls -a`
  - List all files, including hidden dot files.
- `ls -la`
  - List all files with details.

### Folders
- `mkdir name`
  - Create a new folder.
- `mkdir -p a/b/c`
  - Create nested folders all at once.
- `rmdir name`
  - Delete an empty folder.

### Files
- `touch file.txt`
  - Create an empty file.
- `cat file.txt`
  - Display file contents.
- `cp a.txt b.txt`
  - Copy a file.
- `mv old.txt new.txt`
  - Rename or move a file.
- `rm file.txt`
  - Delete a file permanently.
- `rm -r folder`
  - Delete a folder and everything inside permanently.

> ⚠️ `rm` deletes permanently. No undo.

### Writing to Files
- `echo "text"`
  - Print text to the terminal.
- `echo "text" > file`
  - Write text to a file, overwriting existing content.
- `echo "text" >> file`
  - Append text to the end of a file.

### VS Code Commands
- `code .`
  - Open the current folder in VS Code.
- `code file.txt`
  - Open a specific file in VS Code.

### History & Shortcuts
- Up arrow (`↑`)
  - Navigate previous commands.
- `Ctrl+R`
  - Search command history.
- `Tab`
  - Auto-complete file/folder names.
- `Ctrl+C`
  - Cancel a running command.
- `Ctrl+L`
  - Clear the terminal screen.
- `history`
  - Show recent commands.

### Aliases
- `alias`
  - List current aliases.
- `alias ll='ls -la'`
  - Create a temporary shortcut.
- `source ~/.bash_profile`
  - Reload your config file after editing.

### Path Shortcuts
- `~`
  - Your home directory.
- `.`
  - Current directory.
- `..`
  - Parent directory.

### Common Errors
- `No such file or directory`
  - Check for typos or missing paths; run `ls` to verify.
- `Permission denied`
  - You don’t have permission for the action; move to a different folder.
- `command not found`
  - Typo in the command name.
- `too many arguments`
  - Use quotes or escape spaces in folder/file names.
