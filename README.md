# bash-me
Repository for storing my configuration files and easily porting then between devices.

Based on the following guide: https://www.atlassian.com/git/tutorials/dotfiles

## Installation
1. Clone into a bare repository
`git clone --bare https://github.com/TheGreatMarkus/bash-me.git ~/.myconfig`
2. Set the following alias in your terminal session
`alias my-config='/usr/bin/git --git-dir=$HOME/.myconfig/ --work-tree=$HOME'`
3. Checkout the content from the repository to your home directory
`my-config checkout`
You might get warning that the checkout would override existing files. In that case simply back them up or delete them.
4. Hide untracked files
`my-config config --local status.showUntrackedFiles no`

##  Use

### bash

1. Locate your bash profile file:
    * Linux: `~/.bashrc`
    * MacOS: `~/.bash_profile`
2. Paste the following into your bash profile:
```bash
########### <CUSTOM-CHANGES> ###########
if [ -f ~/.custom.bashrc ]; then
    . ~/.custom.bashrc
fi
########### </CUSTOM-CHANGES> ###########
```
3. Enjoy!

### zsh

1. Locate your zsh profile: 
    * Default: `~/.zshrc`
2. Paste the following into your bash profile:
```bash
########### <CUSTOM-CHANGES> ###########
if [ -f ~/.custom.zshrc ]; then
    . ~/.custom.zshrc
fi
########### </CUSTOM-CHANGES> ###########
```
3. Enjoy!