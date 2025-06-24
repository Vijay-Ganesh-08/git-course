# Git Course

- Centralized and Distributed Version Control System
- Single Code Repository used for Collaboration and Version Control
- Everyone in Development team is aligned/aware with the changes
- Local Repository - Local Machine contains git repository and its branches
- Remote Repository - GitHub site which can be used by team to collaborate
- Staging Area - Letting Git know to what files to track; any changes done to the files, we need to add that to staging area and then commit. files which are un-staged can also be committed directly but not recommended.
- Commit History - Tracking the changes in file for all commits, every commit will have an ID of 40 characters (only 7 shown) which helps for rollback and to track the changes applied to the files.
- Git can be cloned and pushed either by HTTPS (Login Creds) or SSH (Public/Private KeyPair)

---

# Git Commands 

- `**git init**` → Creates a local repository in your local machine for the project folder
- `**git init -b main**` → Creates a local repository in your local machine for the project with branch main
    - `main` - branch name
- `**git status**` → To check the status of git repository
- `**rm -rf .git**` → To delete the folder of .git (local git repository) from the project folder
- `**git add FirstCode.txt**` → To add specific file to the staging area of git
    - `FirstCode.txt` - file name
- `**git add .**` → To add all the changed/created files to the staging area of local git repository
- `**git rm --cached FirstCode.txt**` → To remove the specific file from local git repository
    - `FirstCode.txt` - file name
- `**git restore --staged confidential.txt**` → To restore the deleted file to un-staged
- `**git log**` → To check the history of commits done to local git repository
    - It provides commit Id, Author , date and commit message
- `**git log --pretty=oneline**` —> To check the history of commits done to local git repository
    - It provides commit id and message in single line
- `**git commit -m “FirstCommit”**` → To commit the changes in local repository, message is mandatory
    - `-m` —> refers to the message of commit and text inside “” is the commit message
    - `FirstCommit` - commit message
- `**git commit -a -m "Skipping Staging”**` → To commit directly from Modified file without staging
    - `-a` —> refers to add all the modified files to staging area
    - `-m` —> refers to the message of commit and text inside “” is the commit message
- `**git diff**` → To check the changes of the previous staged version and the files changed in working directory
- `**git diff --staged**` → To check the changes happened to the files which is added to staging area.
- `**git clone XXXX.git**`→ To take a copy of code base from remote to local repository.
- `**git branch -M main**` → To mark the working branch as MAIN
- `**git remote add origin XXXXX.git**` → To add the remote repository to the local repository
- `**git push -u origin main →**` To push the code from local repository to remote repository for the first time.
- `**git push origin main**` → To push the code from local repository to remote repository.
    - `origin` → Remote Repository URL
    - `main` → Branch Name to be pushed to
- `**git remote -v**` → To check the remote repositories (For Fetch and to Push)
- `**git tag -a v1.0 -m "Version 1”**` → To add a tag to the source code
    - `v1.0` is the Tag name
    - `Version` 1 is the Tag Message
- `**git push origin v1.0**` → To push the tags to remote repository
- `**git checkout -b feature1**` or `**git switch -c feature1**` → Creates a new branch named `feature1` and switches to this branch as working directory
- `**git checkout main**` or `**git switch main**` → switches/checksout the working directory to branch `main`
- `**git branch**` → To list all the branches from local repository and * is prefixed for check-out or working branch
- `**git branch --all**` → To list all the branches from local and remote repository and * is prefixed for check-out branch in local repository
- `**git switch -**` → To switch the working directory to the previous branch
- `**git branch -d feature2**` → To delete the feature2 branch from local repository
- `**git merge main feature1**` → to Merges the branches
    - `main` - Destination Branch, this should be the working directory
    - `feature1` - which has the latest code which needs to be applied to main
- `**git pull**` → To pull the latest code from remote to local repository for the branch in working directory