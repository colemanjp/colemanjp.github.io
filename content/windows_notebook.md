---
title: "Windows Minibook"
author: "John Coleman"
date: "2025-03-11"
tags: 
     - windows
---

# Windows Packaged Software

- calibre
- chrome
- keepassxc 
- dropbox (from MS store)
- libreoffice
- liquidtext (from MS store)
- neovim
- usbipd-win (so WSL can read USB storage)
- vlc (from MS store)
- zotero

# WSL 

`wsl --update`

`wsl --install kali-linux`

## WSL Kali Packaged Software
- kali-desktop-core (enables graphical applications)
- neovim
- 7zip
- usbutils

`apt install -y kali-desktop-core neovim 7zip usbutils`

## WSL Kali Non Packaged Software
### VeraCrypt

`apt install ./veracrypt-1.26.20-Debian-12-amd64.deb`
