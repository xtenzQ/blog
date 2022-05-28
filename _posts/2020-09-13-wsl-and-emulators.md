---
layout: post
title: "Fixing BSOD while running BigNox and WSL"
date: 2020-09-13 21:42:00 +0100
author: "Nikita Rusetskii"
category: development
image: img/in-post/wsl.jpg
imagecaption: ""
tags: [dev, wsl, linux, windows]
---

Today I have encountered a problem related to running android emulators and Windows Subsystem Linux which was not mentioned in [BigNox BSOD repairing tutorial](https://www.bignox.com/blog/bsodsolutions1/). I was thrown a BSoD every time I run BigNox.

It's not possible to run WSL and BigNox at the same time, but disabling `Virtual Machine Platform` feature helps to solve the problem.
