---
created: 2025-08-06
title: killall
tags:
  - process
  - cli
aliases: 
lang: uk
---

> [!tldr]
> **killall** - команда для надсилання сигналу групі процесів по імені.

```bash
killall [-wdivrg] [-u user] [-t term] [-SIG] [-s SIG] [name ...]
```

##  Опції

- `-i` - інтерактивно
- `-r` - name як [[Регулярні вирази|regexp]]
- `-u user` - тільки процеси заданого користувача
- `-w` - чекати завершення
- `-s SIG` - відправити сигнал
