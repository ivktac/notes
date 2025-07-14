---
date: 2025-07-10
title: ps
description: 
draft: false
tags:
  - os/process
  - os/cli
  - man
aliases: 
permalink: 
lang: uk
---

> [!tldr]
> **ps** дозволяє отримати моментальний знімок процесів.


## Опції

- `w`: широкий формат
- `a`: процеси усіх користувачів
- `x`: всі процеси незалежно від TTY
- `o fields`: конкретні поля
- `u`: типовий набір полів

> [!example] Вивести тільки PID і команду
> 
> ```bash
> ps axo pid,command
> ```

## Основні поля

- USER, PID, %CPU, %MEM
- VSZ (віртуальний розмір)
- RSS (реальний розмір)
- TTY, STAT, START, TIME, COMMAND

## Див. також

- [[Процес]]
- [[Атрибути процесів]]
- [[top]]
- [[pstree]]