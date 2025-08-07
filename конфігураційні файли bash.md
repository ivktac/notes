---
created: 2025-08-06
title: конфігураційні файли bash
tags:
  - bash
  - config
aliases:
  - bash configuration
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
