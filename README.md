# .dotfiles

## Overview

This repo contains my dotfiles for my Ubuntu installation

## Prerequisites

```bash
sudo apt install neovim ripgrep stow -y
```

## Shell

Install zsh:

```bash
sudo apt install zsh -y
```

Install Oh My Zsh:

```bash
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```
Allow the default shell to be zsh then confirm shell is set to zsh:

```bash
echo $SHELL
```
## Installing Dotfiles

```bash
cd ~
git clone --recursive https://github.com/jarossnd/.dotfiles
cd .dotfiles
```

Set executable permissions on the install scripts:

```bash
chmod 755 install
chmod 755 ubuntu
```

Run the ubuntu script to stow files

```bash
./ubuntu
```
## Install Packer for Neovim

```bash
git clone --depth 1 https://github.com/wbthomason/packer.nvim\
 ~/.local/share/nvim/site/pack/packer/start/packer.nvim
```
## Run PackerSync

```bash
cd ~/.config/nvim/lua/jaross
nvim packer.lua
:so
:PackerSync
```



