---
title: "Autorize Walkthrough"
author: "John Coleman"
date: "2025-10-14"
draft: false
tags: 
     - walkthrough
     - burp
     - docker
---
# Instructions 
Black Hills Information Security: [Finding Access Control Vulnerabilities with Autorize](https://www.blackhillsinfosec.com/finding-access-control-vulnerabilities-with-autorize/)

# Run Juice-Shop in Docker Rootless

- `systemctl --user start docker`
- `docker context use rootless`
- `docker run --rm -p 8000:3000 bkimminich/juice-shop`

# Set up Firefox
- `firefox --no-remote -p`
- Create Primary and Secondary profiles
- Install foxy-proxy
- Add Burp proxy type in foxy-proxy
- Edit about:config to allow firefox proxying for localhost
	- network.proxy.allow_hijacking_localhost
	- network.proxy.testing_localhost_is_secure_when_hijacked

# Log in as admin on Primary Firefox
`admin@juice-sh.op`

`admin123`
# Upload a Profile Picture
This would be an activity that should require auth and authz
# Send the Profile Upload to Burp Repeater
Remove cookies to find which are required for auth
# Log in as mc.safesearch on Secondary Firefox 
`mc.safesearch@juice-sh.op`

`Mr. N00dles`
# Paste the JWT from this low Privilege Account into Autorize 
# Enable Autorize
