# GIT-COMMANDS
This repository only contains commands related to GIT

**Good Reads :**<br>
1 . [Kernel](https://mirrors.edge.kernel.org/pub/software/scm/git/docs/gittutorial.html)    

----------------------------------------------Git Commands--------------------------------------------------------
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
- [GIT DIFF EXPLAINATION](https://stackoverflow.com/questions/3686452/what-are-the-differences-between-these-git-diff-commands/3686507#3686507)
- In order to directly commit changes without adding to staging area it can be done using :
    *   **git add -a -m "commit message"**
- To remove a file from being tracked by git :
    *   **git rm path-to-filename**
    *   **git rm --cached path-to-filename** (To remove file that has been staged and will be untracked by git) 
- To rename file in git :
    * **git mv file_from file_to**
- VIEWING GIT COMMIT HISTORY :
    * **git log -p -2** : -p shows difference introduced in each commit, -2 limits output to only last two commits
    * **git log --stat** : gives out some abbreviated stats for each commit
    * **git log --pretty=oneline**
    * **git log --graph** : gives a ascii graph representation of branch and merge history
- UNDOING THINGS :
    * When you commit too early and forgot to add some files :
    * **git commit --amend**
    SCENARIO :<br> 
    1 . Made a commit using : git commit -m "Initial commit"<br>
    2 . Forgot to add file : git add forgot_file <br>
    3 . Amend comit : git commit --amend <br>
    Ends up with single commit second commit replaces result of first .<br>
- UNSTAGING STAGED FILES :
    * Lets say we added all files that are changed in our working directory using **git add .**, later on realized one of the<br>
    staged file needs to be unstaged or is not required to commit .
    * **git reset HEAD <file_name>**
    * To unstage all staged files .
    * **git reset**
- TO REPLACE FILE WITH HEAD REVISION :
    * **git checkout -- path_to_file_replacement**
- SHOWING REMOTES :
    * **git remote**    : Lists shortname of all remote servers handled .
    * **git remote -v** : Lists URLs for shortnsmes git has configured .
- ADDING GIT REMOTE :
    * **git remote add <remote_name> <remote_URL>** : In order to add new remote wiht name and url .
- FETCHING AND PULLING FROM YOUR REMOTES :
    * **git fetch <remote_name>** : Automatically fetches any new work that has been to remote since last update, but it doesnt 
    merge with any of your work .
    * **git pull** : It is used to automatically fetcha and merge
- PUSHING TO YOUR REMOTES :
    * **git push <remote_name> <branch_name>** : 
- INSPECTING REMOTE :
    * **git remote show <remote_name>** : Gives info about remote
- TAGGING :
    * GIT has the ability to tag specific points in history . Typically people use tag functionality to mark release points .
    * **git tag** : This command lists all tags in alphabetical order
    * If GIT source repo has more tags in order to search for tags we can use patterns :
    * **git tag -l 'v1.8.5.*'**  : Lists all tags whose name starts with v1.8.5
    * GIT uses two types of tags : annotated tag and lightweight tag
    
- GIT ALIASES : 
    * If we dont want to type entire text of each git commands , we can setup alias for each git command .
    * **git config --global alias.co checkout** : Instead of typing checkout , type co which does the same
    * **git config --global alias.br branch**
    * **git config --global alias.ci commit**
    * **git config --global alias.st status**
    * **git config --global alias.unstage 'reset HEAD --'**
    * **git config --global alias.last 'log -1 HEAD'**
 
 - GIT BRANCHING :
    *  The “master” branch in Git is not a special branch. It is exactly like any other branch. The only reason nearly
    every repository has one is that the git init command creates it by default and most people don’t bother to change it.
    * **git branch `<branch-name>`** :  creates a new pointer at the same commit you’re currently on .
    * **git checkout `<branch-name>`** : moves HEAD pointer to target branch-name .
    
    
    
    
        
    
    
