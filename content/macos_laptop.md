---
id: macos_laptop
aliases: []
tags:
  - macos
  - nix
author: "John Coleman"
date: 2026-11-17
draft: false
title: "MacOS Laptop"
---

# Install Software from Packages (running list)
- Anki
- Dropbox
- FalconSensor
- Keepassxc
- MS Teams (MS download)
- MS Todo (App Store)
- Syncthing (https://syncthing.net/downloads/)
- Vivaldi
- Xmind
- Zettlr

# Install Software from Nix

## Download and Install Determinate.pkg
https://docs.determinate.systems/getting-started/individuals/

## Search
`nix search nixpkgs ^neovim$`

## Install in Shell Only
`nix shell nixpkgs#neovim`

## Install Permanently (running list)
```
nix profile add nixpkgs#neovim
nix profile add nixpkgs#ghostty-bin
nix profile add nixpkgs#stow
nix profile add nixpkgs#bashInteractive
nix profile add nixpkgs#texstudio
nix profile add nixpkgs#texliveFull
nix profile add nixpkgs#ripgrep
nix profile add nixpkgs#openvpn
nix profile add nixpkgs#remmina
nix profile add nixpkgs#gowitness
nix profile add nixpkgs#fzf
nix profile add nixpkgs#tigervnc
nix profile add nixpkgs#awscli2
```


## Install Logseq
Complains about Electron dependency

`NIXPKGS_ALLOW_INSECURE=1 nix profile add --impure nixpkgs#logseq`

## Show Installed
`nix profile list`

## Flakes
Need to explore

`nix run "https://flakehub.com/f/DeterminateSystems/fh/0" -- init`

# Ghostty Configuration
## Run bash when you start ghostty

~/.config/ghostty/config

```
command = /Users/username/.nix-profile/bin/bash
```
