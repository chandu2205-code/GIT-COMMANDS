# GIT-COMMANDS
This repository only contains commands related to GIT

- **git config --list**
- **git config user.name="type your name here"**
- **git config user.email="enter your email here"**
- **git add (*).c**
- **git add LICENSE**
- **git commit -m "commit message"**
- **git clone URL**
- **git clone URL dest_directory** [Target Directory to which changes should be cloned]
- Terminology related to life cycle status of different files : Untracked, Tracked --- Tracked further can be staged,unmodified,modified
- **git status**
- **git status -s or git status --short**
- To create .gitignore files : <br>
    1 . **cat .gitignore**<br>
        -> *.[oa]  ............. tells ignore any files ending in .o or .a<br>
        -> *~ .................. tells git to ignore all files that end with tilde<br>
        -> *.a ................. tells git to ignore all files that end with .a<br>
        -> !lib.a .............. but do track lib.a , even though you are ignoring .a files above<br>
        [For MORE INFO ON GIT IGNORE](https://github.com/github/gitignore)

- **git diff** [differentiates between working directory & staging directory]
- **git diff --staged** [differentiates between staged changes and last commit]
