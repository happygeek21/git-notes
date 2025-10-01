

VERSION CONTROL SYSTEM (VCS)
----------------------------
- A repository is like a database that stores files and tracks changes.
- You can view history (who made changes, when).
- You can revert to earlier versions.
- Makes it easy to track versions and work together.

TYPES OF VCS
------------
1. Centralized:
   - Shared repository (single server).
   - Problem: Single point of failure if server goes down.

2. Distributed:
   - Each user has a full copy of the project locally.
   - Work offline, then sync with others.
   - No single point of failure.

WHY GIT
-------
- Free & Open Source
- Super fast & scalable
- Widely used, important for jobs
- Makes collaboration and history tracking easy

USING GIT
---------
- Command Line (CLI) → Best and always available
- IDEs (like VS Code) → Built-in Git support
- Extensions: GitLens for VS Code
- GUIs:
  - GitKraken (Windows/Linux/Mac)
  - SourceTree (Windows/Mac only)
- Tip: Use CLI mainly, GUI when needed for speed

INSTALLING GIT
--------------
- Check version: git --version
- On Windows: Git Bash is preferred over default CMD

CONFIGURING GIT
---------------
3 Levels of config:
1. System - All users
2. Global - All repos of current user
3. Local - Only current repo

Set username and email:
==git config --global user.name "yourname"==
==git config --global user.email "youremail@example.com"==

Set default editor (example VS Code):
==git config --global core.editor "code --wait"==

Edit global settings:
==git config --global -e==

Handling End of Line (EOL):
Windows uses \r\n
Mac/Linux uses \n
==git config --global core.autocrlf true     (Windows)==
==git config --global core.autocrlf input    (Mac/Linux)==

GETTING HELP
------------
==git config --help==
==git config -h==

INITIALIZING A REPO
-------------------
git init
(Creates .git hidden folder with config, objects, refs etc.)
WARNING: Deleting .git removes history!

BASIC GIT WORKFLOW
------------------
Local Project → Staging Area → Repository

- Staging = Prepare and review changes
- Commit = Save snapshot to repository

EXAMPLES
--------
Add and commit:
==git add file1 file2==
==git commit -m "Meaningful message"==

Remove if deleted locally:
==git add file2==
==git commit -m "Removed unused code"==

COMMITS
-------
Each commit has:
- ID
- Message
- Author
- Date/Time
- Snapshot
(Note: Git compresses and avoids duplicate storage)

TRACKING FILES
--------------
==echo hello1 > file1.txt==
==echo world >> file2.txt==

Symbols in git status:
? = Untracked file
+ (yellow) = Staged but not committed
Green = Synced with repo

Check status:
==git status==
==git status -s (short view)==

COMMITTING CHANGES
------------------
==git commit==
==git commit -m "message"==

Skip staging (not recommended):
==git commit -am "message"==

FILE OPERATIONS
---------------
Remove file:
==rm filename==              (only locally)
==git rm filename==          (local + staging)

Rename/move:
==git mv old_filename new_filename==

IGNORING FILES
--------------
1. Create .gitignore
2. Add rules (example):
   /directory_name
   *.log
3. Remove from repo:
==git rm --cached -r /directory_name==
==git commit -m "ignored files"==

BEST PRACTICES
--------------
- Commit often
- Use meaningful commit messages (present tense)
- Stage changes clearly
- Mix CLI and GUI as needed

===============================
