---
title: "Restic Cheatsheet"
author: "John Coleman"
date: "2025-01-17"
tags: 
     - cheatsheet
---

# Create repo
`restic init --repo /path/mybackups`
# Manage snapshots
## List files in latest snapshot
`restic -r /path/mybackups ls latest`
## Delete single snapshot
`restic -r /path/mybackups snapshots`

`restic -r /path/mybackups forget mysnapshotID`

`restic -r /path/mybackups prune`
# Check backups
`restic -r /path/mybackups check --read-data`
# Purge excluded files from historical backups
`restic -r /path/mybackups --verbose rewrite --forget --exclude-file myexclude.txt --dry-run`

`restic -r /path/mybackups --verbose rewrite --forget --exclude-file myexclude.txt`

`restic -r /path/mybackups prune`
# Simple backup script with hardcoded password
```
#!/bin/sh 
export RESTIC_PASSWORD=YOURPASSWORDHERE
restic -r /mnt/backups --verbose backup ""$HOME" --exclude-file ""$HOME"/.restic/exclude.txt
```
