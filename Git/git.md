
<p align="center">
	<img src="https://github.com/Saurav-Paul/My-Wiki/blob/master/logo.png" align="center" >
</p>

<h1 align="center">my wiki</h1>
<h4 align="center"><i>Informations & tutorials</i> </h4>

---


## Git Commands

 ---
 
_A list of my commonly used Git commands_

--

### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |



## Bare git

**The commands need for bare git are given below**

>git init --bare $HOME/dotfiles

> alias config='/usr/bin/git --git-dir=$HOME/dotfiles/ --work-tree=$HOME' (add this alias to .bashrc)

**Then reload your bash and type on terminal**

config config --local status.showUntrackedFiles no


**Basic usage example:**

add : 
>config add /path/to/file

commit:
>config commit -m "A short message"

push :
>config push


*WHAT'S THE REASON FOR THE GIT BARE REPO?

By using the git bare repo, you can have nested git repos in your home directory and there will not be any issue with keeping things straight.   That is the reason for the git bare repo and having an alias ("config").*



## How to stop asking for username or password everytime ?


#### Entering Git Username and Password in Remote URL

```bash

$ sudo git clone https://username:your_password@github.com/username/repo_name.git

OR

$ sudo git clone https://username:your_password@github.com/username/repo_name.git local_folder

```
drawback : The main drawback of this method that your username and password will be saved in the command in the Shell history file and .git/config file.

### Saving Remote Git Repository Username and Password on Disk
```bash
$ git config credential.helper store				

OR

$ git config --global credential.helper store	
```

**From now on, Git will write credentials to the ~/.git-credentials file for each URL context, when accessed for the first time.**

To view the content,

```bash
$ cat  ~/.git-credentials

```

### Caching Remote Git Repository Username and Password in Memory

*Last but not least, you can also use the Git credentials helper to temporarily save your credentials in memory for some time. To do that, issue the following command.*

```bash
$ git config credential.helper cache
OR
$ git config --global credential.helper cache

```

*After running the above command, when you try to access a remote private repository for the first time, Git will ask for your username and password and save it in memory for some time.*

*The default caching time is 900 seconds (or 15 minutes), after which Git will prompt you to enter your username and password again. You can change it as follows (1800 seconds = 30 minutes or 3600 seconds = 1hour).*



```bash
$ git config --global credential.helper 'cache --timeout=18000'
OR
$ git config --global credential.helper 'cache --timeout=36000'
```
