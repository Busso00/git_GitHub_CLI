# Git fundamentals

## NewREPO

Create ".git" folder
```sh
    git init
```

## Staging area
Show which file will be considered in next commit
```sh
    git status
```

### Add
Add changes (specified file or folders) into staging area (add to to-commit area)
```sh
    git add .
```
or
```sh
    git add DirName/FileName.ext
```
### Remove
Remove from staging area
```sh
    git rm --cached
```

### Reset
Remove stage changes from staging area (remove from to-commit area)
```sh
    git reset
```




## Clone

### HTTPS

For public repo
```sh
git clone https://github.com/USER_NAME/REPO_NAME.git
```

To push you need a PAT (Personal Access Token)

#### Personal access tokens
Get it for a repo you own and share it to who need access.
Paste it instead of password for an authenticated operation on a repo.


### SSH
For private repo
```sh
git clone git@github.com:USER_NAME/REPO_NAME.git
cd REPO_NAME
```
Create SSH-keygen create public (and private key)
```sh
    sshe-keygen -t rsa
```
Save in an absolute path out of GitHub folder and print it with:
```sh
    cat /PATH/TO/MY/RSAKEY.pub
```
Copy the full output to SSH key add in your profile GitHub SSH's section (from profile -> settings -> SSH & GPG) paste it and save it.

### GitHub CLI

Install CLI on your machine.

Can upload your SSH key authomatically detected on your system if you use select SSH.


## Commits
Commit with a message (without -m it opens default editor to write message)
```sh
   git commit -m "message that specify your changes"
```
### Set default editor, name, email
Set editor, name, email locally (in .gitconfig in current directory)
```sh
    git config core.editor YOUR_EDITOR_EXE
    git config user.email "your_email@example.com"
    git config user.name "Name Surname"
```
Show git variables
```sh
    git config --list
```

## Branches

List of branches:
```sh
    git branch
```

