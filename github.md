# Dotfiles bare repo from scratch

**Creating bare repo directory:**

  1. `mkdir dotfiles`

  2. `cd dotfiles`

  3. `git init --bare $HOME/dotfiles`


  4. `alias config='/usr/bin/git --git-dir=$HOME/dotfiles/ --work-tree=$HOME'`
  
**Adding alias to .bash_aliases**
 
  5. `config config --local status.showUntrackedFiles no`
 
**Adding dotfiles to github repo**
 
  6. `config add "file/directory"`
 
  7. `config commit -m "remarks"` 
 
  8. `config push "git URL"` 
*if rejected error try adding -f -u after push*

---

# Dotfiles migration to new system
