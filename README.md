Dotfiles
========

This is my dotfile repository. There are many like it, but this one is mine.

 - [Installation](#installation)
 - [Vim](#vim)
 - [Xmonad](#xmonad)

## Installation

With `git` and `curl` installed, run the command below from the home directory. This will clone the dotfiles repository and run the bootstrap script.

```
git clone https://github.com/JDevlieghere/dotfiles.git ~/dotfiles && source ~/dotfiles/bootstrap.sh
```

## Vim

Vim is my editor of choice and I've tweaked my configuration quite a bit to make it fit my particular needs. Today it's used mainly for C++ development. I use [Vundle](https://github.com/VundleVim/Vundle.vim) to manage my plugins. You can have a look at the respective repositories to discover what each of them does. 

### YouCompleteMe

One plugin worth mentioning is [YouCompleteMe](https://github.com/Valloric/YouCompleteMe) as it requires some attention to install, so make sure to check its documentation. 

For semantic completion it [requires](https://github.com/Valloric/YouCompleteMe#c-family-semantic-completion-engine-usage) an addition configuration file `.ycm_extra_conf.py` containing project specific compilation flags. I use a global file that looks for a `include` directory and a `.clang_complete` file in the current working directory or in any directory above it in the hierarchy. It then reads the compile flags from the `.clang_complete` file and adds `-I` flags all subdirectories of the nearest `include` folder. 

## Xmonad

When I got started with xmonad I came across [Vic Fryzel's configuration](https://github.com/vicfryzel/xmonad-config) which I grew fond of over time.  It is still largely the same, except for a few small changes here and there. 