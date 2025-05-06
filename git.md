# Git setup (clone and auth)

## HTTPS

For public repo
```sh
git clone https://github.com/USER_NAME/REPO_NAME.git
```

To push you need a PAT (Personal Access Token)

#### Personal access tokens
Get it for a repo you own and share it to who need access.
Paste it instead of password for an authenticated operation on a repo.


## SSH
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

## GitHub CLI

Install CLI on your machine.

Can upload your SSH key authomatically detected on your system if you use select SSH.


## Set default editor, name, email
Set editor, name, email locally (in .gitconfig in current directory):
```sh
git config core.editor YOUR_EDITOR_EXE
git config user.email "your_email@example.com"
git config user.name "Name_Surname"
```
Show git variables:
```sh
git config --list
```

# Local git (no history)

Create ".git" folder:
```sh
git init
```

## Staging area
Show which file will be considered in next commit:
```sh
git status
```

### Add
Add changes (specified file or folders) into staging area (add to to-commit area):
```sh
git add .
```
or
```sh
git add DirName/FileName.ext
```
### Remove
Remove from staging area:
```sh
git rm --cached DirName/FileName.ext
```

### Reset
Remove stage changes from staging area (remove from to-commit area):
```sh
git reset
```

## Commits
Commit with a message (without -m it opens default editor to write message):
```sh
git commit -m "message that specify your changes"
```


# Git workflow

NOTE: switch and checkout are similar but checkout is suggested when allowed since can handle revert to old commit. Next section is for command interactions with remote origin.


## Pull
Pull from BRANCH_NAME and merge into current local branch:
```sh
git pull origin BRANCH_NAME
```
runs:
```sh
git fetch origin BRANCH_NAME
git merge origin/BRANCH_NAME
```

## Push
Push to a branch:
```sh
git push -u origin BRANCH_NAME
```

## Branch

List of local branches:
```sh
git branch
```

Create new branch (locally):
```sh
git branch BRANCH_NAME
```

List of remote and local branches:
```sh
git branch -a
```



## Switch

Switch to a branch (locally):
```sh
git switch BRANCH_NAME
```
Switch to a newly created branch:
```sh
git switch -c NEW_BRANCH_NAME
```


## Checkout
Checkout to a specific commit identified by HASH (update files in working directory):
```sh
git checkout HASH
```
Checkout (switch to a specific branch's last commit):
```sh
git checkout BRANCH_NAME
```
Checkout to a newly created branch:
```sh
git checkout -b NEW_BRANCH_NAME
```

## Merge
Merge target BRANCH_NAME into current branch
```sh
git merge BRANCH_NAME
```

## Add remote upstream
```sh
git remote add UPSTREAM_REPO https://LINK_TO_UPSTREAM_REPO
```

## Tagged commit
```sh
git add .
git commit -m "..."
git tag 1.0.0
git push --tags
```

## Checkout to a tagged commit
```sh
git checkout tag
```

## Delete a tag locally
```sh
git tag -d 1.0.0
```

## Delete a tag on remote 
```sh
git push --delete origin 1.0.0
```
