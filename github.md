# Dotfiles bare repo from scratch

Reference: https://www.youtube.com/watch?v=gsO0-wk3yz8

**Creating bare repo directory:**

  1. `mkdir dotfiles`

  2. `cd dotfiles`

  3. `git init --bare $HOME/dotfiles`

**Adding alias to .bash_aliases:**

  4. `alias config='/usr/bin/git --git-dir=$HOME/dotfiles/ --work-tree=$HOME'`
  
  5. `config config --local status.showUntrackedFiles no`
 
**Adding dotfiles to github repo:**
 
  6. `config add "file/directory"`
 
  7. `config commit -m "remarks"` 
 
  8. `config push "git URL"` 
*if rejected error try adding -f -u after push*

**Done.**

# Dotfiles migration to a new system

Reference: https://www.atlassian.com/git/tutorials/dotfiles

**Adding alias to .bash_aliases:**

  1. `alias config='/usr/bin/git --git-dir=$HOME/dotfiles/ --work-tree=$HOME'`

**Ignore the folder where you'll clone it:**

  2. `echo "dotfiles" >> .gitignore`
  
**Now clone your dotfiles into a bare repository directory:**

  3. `git clone --bare https://github.com/SheetaI/dotfiles $HOME/dotfiles`

**Define the alias in the current shell scope:**

  4. `alias config='/usr/bin/git --git-dir=$HOME/dotfiles/ --work-tree=$HOME'`

**Checkout the actual content from the bare repository to your $HOME:**

  5. `config checkout`

**The step above might fail with a message like:**
  
    *error: The following untracked working tree files would be overwritten by checkout:
       .bashrc
        .gitignore
    Please move or remove them before you can switch branches.
    Aborting*

This is because your $HOME folder might already have some stock configuration files which would be overwritten by Git. 

**The solution is simple:** back up the files if you care about them, remove them if you don't care.

**Re-run the check out if you had problems:**

  6. `config checkout`

**Set the flag showUntrackedFiles to no on this specific (local) repository:**

  7. `config config --local status.showUntrackedFiles no`

**Done, from now on you can now type config commands to add and update your dotfiles**


# Git Commands

**User settings**

  - `git config --global user.name SheetaI`
  
  - `git config --global user.email im.kawaii.gg@gmail.com`

**Save credentials**

  `git config --global credential.helper cache`

**Remove saved credentials**

  `git config --global --unset credential.helper`
  
**Configuring new repo**
 
   - `git init` initialize repo to be done once!
  
   - `git status` check if your repo dir is on branch master

 **Update changes to repo**
 
   - `git add .` shows changes were made in red
   
   - `git status` shows changes are added in green
   
   - `git commit -m "remarks"` commit changes
   
   - `git push "insert-git-url" master` or `git push origin master` if the url is aliased
   
 **Git URL aliasing**
 
 - `git remote add origin "insert-git-url"` alias url to remove typing the url all the time
 
 - `git push -u origin master` -u syntax to be done once!
   
