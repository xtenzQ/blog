---
layout: post
title: "Fixing BSOD while running BigNox and WSL"
date: 2020-09-13 21:42:00 +0100
author: "Nikita Rusetskii"
category: development
image: https://i.imgur.com/PkvW7FD.jpg
imagecaption: ""
tags: [dev, wsl, linux, windows]
---

Today I have encountered a problem related to running android emulators and Windows Subsystem Linux which was not mentioned in [BigNox BSOD repairing tutorial](https://www.bignox.com/blog/bsodsolutions1/). I was thrown a BSoD every time I run BigNox.

{% include pic.html url="https://i.imgur.com/hgxZhvv.jpg" description="Windows Features" %}

After a couple of tries I figure out that disabling `Virtual Machine Platform` feature helped to solve the problem.