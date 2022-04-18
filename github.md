## Creating bare repo from scratch

`mkdir dotfiles`

`cd dotfiles`

`git init --bare $HOME/dotfiles`

 - **add bash_aliases:** 
 `alias config='/usr/bin/git --git-dir=$HOME/dotfiles/ --work-tree=$HOME'`
