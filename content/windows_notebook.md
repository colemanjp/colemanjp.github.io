---
title: "Windows Minibook"
author: "John Coleman"
date: "2025-03-30"
tags: 
     - windows
     - WSL
     - neovim
     - ansible
---

# Windows Packaged Software

- anyconnect vpn
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
- neovim
- openvpn
- rawtherapee
- spotify (from MS store)
- usbipd-win (so WSL can read USB storage)
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

### Nvim kickstart

`git clone git@github.com:colemanjp/kickstart.nvim.git "${XDG_CONFIG_HOME:-$HOME/.config}"/nvim`


