# My notes about using git

## git






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


