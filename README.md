# Git fundamentals

## NewREPO

Create ".git" folder
```sh
    git init
```

### Staging area status
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
git clone https://github.com/REPO_NAME.git
```

### SSH
For private repo
```sh
git clone https://github.com/REPO_NAME.git
cd REPO_NAME
```
Create SSH-keygen
```sh
    sshe-keygen -t rsa
```
Test connection
```sh
    ssh -T git@github.com
```

### GitHub CLI


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

## Branches

