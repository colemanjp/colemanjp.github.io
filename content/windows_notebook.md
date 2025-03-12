---
title: "Windows Minibook"
author: "John Coleman"
date: "2025-03-11"
tags: 
     - windows
---

# Windows Packaged Software

- chrome
- keepassxc 
- dropbox (from MS store)
- libreoffice
- zotero
- usbipd-win (so WSL can read USB storage)

# WSL 

`wsl --install kali-linux`

## WSL Kali Packaged Software
- kali-desktop-core (enables graphical applications)
- libfuse2t64 (needed for non deb veracrypt)
- neovim
- 7zip

## WSL Kali Non Packaged Software
### VeraCrypt

`apt install ./veracrypt-1.26.20-Debian-12-amd64.deb`

veracrypt-1.26.20-setup-gui-x64 also works if you install libfuse2t64 first.
