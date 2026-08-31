---
title: "Nvim-Orgmode"
author: "John Coleman"
date: "2025-09-07"
tags: 
     - howto
     - neovim
---

# Alias nvim-orgmode commands in .bashrc

```
alias task="nvim -c 'lua require(\"orgmode\").action(\"capture.prompt\")'"
alias agenda="nvim -c 'lua require(\"orgmode\").action(\"agenda.prompt\")'"
```
