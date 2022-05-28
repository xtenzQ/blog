---
layout: post
title: KeePassXC Ubuntu 22.04 with Google Drive sync
author: Nikita Rusetskii
date: 2022-05-26 16:04 +0800
tags: [linux, googledrive]
---

So, the first question is what should I choose? `rclone` or `google-drive-ocamlfuse`?
Well, they both use FUSE file system and if you want to sync Google Drive, `google-drive-ocamlfuse` is less pain in the ass. Actually, after spending two hours setting up `rclone` and then configuring a service on startup, I found out KeePassXC can't load the `.kdbx` from the mounted point. Seems like it's required to copy the db file from the mount to local storage so `google-drive-ocamlfuse` is really a way since it does everything for you. Let's start.

# Installation

Just follow the official docs:

Install with:
```bash
sudo add-apt-repository ppa:alessandro-strada/ppa
sudo apt-get update
sudo apt-get install google-drive-ocamlfuse
```

Authorize to Google Drive running this command for the first time:
```bash
google-drive-ocamlfuse
```

Create the mount point:
```bash
mkdir ~/mygoogledrive
```
Mount the filesystem:
```bash
google-drive-ocamlfuse ~/mygoogledrive
```

To speed up the ocamlfuse, try increasing value of `metadata_cache_time` from `60` to `600` in the config file:
```bash
vim ~/.gdfuse/default/config
```

Copy your `.kdbx` to your Google Drive, and open it in KeePassXC.

**Enjoy! :)**