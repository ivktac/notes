---
date: 2025-07-10
title: killall
description: 
draft: false
tags:
  - os/process
  - man
aliases: 
permalink: 
lang: uk
---

> [!tldr]
> **killall** - команда для надсилання сигналу групі процесів по імені.

## Синтаксис

```bash
killall [-wdivrg] [-u user] [-t term] [-SIG] [-s SIG] [name ...]
```


##  Опції

- `-i` - інтерактивно
- `-r` - name як [[Регулярні вирази|regexp]]
- `-u user` - тільки процеси заданого користувача
- `-w` - чекати завершення
- `-s SIG` - відправити сигнал

> [!example] Надіслати усім процесам `man` `HUP`
> `killall -s 1 man`

## Див. також

- [[kill]]
- [[nice]]