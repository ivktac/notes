---
created: 2025-08-06
title: як отримати статистику по використанню inode у файловій системі?
tags:
  - how-to
aliases: 
lang: uk
---


```bash
$ df -i
```

Результат:

```bash
Filesystem            Inodes  IUsed    IFree IUse% Mounted on
devtmpfs              952605    379   952226    1% /dev
tmpfs                 958203      1   958202    1% /dev/shm
tmpfs                 819200    579   818621    1% /run
/dev/mapper/ol-root 23617536 122982 23494554    1% /
/dev/sda1             524288    379   523909    1% /boot
tmpfs                 191640     15   191625    1% /run/user/1000
```