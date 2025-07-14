---
date: 2025-07-14
title: Конфігураційні файли bash
description: 
draft: false
tags:
  - os/🐧linux
  - os/cli
  - programming/bash
  - configuration
aliases: 
permalink: 
lang: uk
---


## Сесії оболонки входу (interactive shell)

- `/etc/profile` — глобальний скрипт конфігурації
- `~/.bash_profile` — особистий файл запуску користувача
- `~/.bash_login` — якщо `~/.bash_profile` відсутній, тоді прочитати цей скрипт
- `~/.profile` — ні `~/.bash_profile`, ні `~/.bash_login` не знайдено, тоді прочитати цей файл

## Сесії оболонки без входу (non-interactive shell)

- `/etc/bash.bashrc` — глобальний скрипт конфігурації
- `~/.bashrc` — особистий файл запуску користувача
