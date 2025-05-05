## Install GitHub CLI for Linux
Run
```sh
(type -p wget >/dev/null || (sudo apt update && sudo apt-get install wget -y)) \
	&& sudo mkdir -p -m 755 /etc/apt/keyrings \
        && out=$(mktemp) && wget -nv -O$out https://cli.github.com/packages/githubcli-archive-keyring.gpg \
        && cat $out | sudo tee /etc/apt/keyrings/githubcli-archive-keyring.gpg > /dev/null \
	&& sudo chmod go+r /etc/apt/keyrings/githubcli-archive-keyring.gpg \
	&& echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
	&& sudo apt update \
	&& sudo apt install gh -y
```
then
```sh
sudo apt update
sudo apt install gh
```

### Login
```sh
gh auth login
```

### Create repo
```sh
gh repo create NEW_REPO_NAME
```

### Delete repo
```sh
gh repo delete REPO_NAME
```

### View current repo
```sh
gh repo view
```

### Fork repo
Fork allow to create a new repo from one hosted by another OWNER under your own ownership (tree is unchanged)
NOTE: your push will go to your own repo, to merge to main you need a PR
```sh
gh repo fork ORIGINAL_OWNER/REPO_NAME
```

## Pull request
### Create PR
```sh
gh repo set-default ORIGINAL_OWNER/REPO_NAME
gh pr create
```

### List PR
```sh
gh pr list
```

### Merge PR
```sh
gh pr merge PR#
```

## Issue

### Create issue
```sh
gh issue create --title "TITLE" --body "BODY"
```

### List issues
```sh
gh issue list
```

### Delete issue
```sh
gh issue delete ISSUE#
```