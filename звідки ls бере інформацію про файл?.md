---
date: 2025-07-03
title: Звідки ls бере інформацію про файл?
description: 
draft: 
tags:
  - man
  - os/filesystem
aliases: 
permalink: how-command-ls-works
lang: uk
---

Майже вся інформація для виводу при  `ls` (зокрема для `ls -l`) береться з [[Метадані файлу (inode)]] за допомогою виклику [[stat]], але окрім:
 - _ім'я файлу_ — з поточної директорії
- _імена власника_ та _групи_ — конвертуються по ідентифікатору з inode (`/etc/passwd` по [[UID]], `/etc/group` по [[GID]])

## Див. також

- [[ls -l explain|пояснення ls -l]]
