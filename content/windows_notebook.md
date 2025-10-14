---
title: "Windows Minibook"
author: "John Coleman"
date: "2025-10-14"
tags: 
     - windows
     - WSL
     - neovim
     - ansible
---

# Windows Packaged Software

- anki
- anyconnect vpn
- apple devices (from MS store)
- calibre
- chrome
- digikam
- keepassxc 
- dropbox (from MS store)
- git (from git-scm.com default install)
- jre-8u441-windows-x64 (from Oracle. Needed by libreoffice)
- ledger live desktop
- libreoffice
- liquidtext (from MS store)
- openvpn
- rawtherapee
- spotify (from MS store)
- standard notes
- syncthing
- usbipd-win (so WSL can read USB storage)
- vivaldi
- vlc (from MS store)
- zotero

# WSL

## WSL Kali Install

`wsl --update`

`wsl --install kali-linux`

## WSL Kali Install Packaged Software

`sudo apt update`

`sudo apt install ansible-core`

`cd && git clone git@github.com:colemanjp/ansible_playbooks.git ansible`

`sudo /bin/ls`

`ansible-playbook ansible/roles/wsl/tasks/main.yml  --connection=local --check`

`ansible-playbook ansible/roles/wsl/tasks/main.yml  --connection=local`

## WSL Kali Non Packaged Software
### VeraCrypt

`apt install ./veracrypt-1.26.20-Debian-12-amd64.deb`

### Install stow dotfiles

`git clone git@github.com:colemanjp/stow-dotfiles.git "${HOME}/.dotfiles`

### Neovim from App image

Packaged version in Kali doesn't support nvim-orgmode

`curl -LO https://github.com/neovim/neovim/releases/latest/download/nvim-linux-x86_64.appimage`
