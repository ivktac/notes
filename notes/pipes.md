---
date: 2025-07-05
title: Конвеєри (Pipes)
description: 
draft: false
tags:
  - os/process
  - os/🐧linux
aliases:
  - pipe
  - pipes
permalink: linux-pipes
lang: uk
---
> [!tldr]
> **Конвеєр (pipes)** - це міжпроцесерна взаємодія, яка дозволяє процесам перенаправляти потоки.

##  Принцип роботи

> [!info] Принцип роботи
> - **STDOUT** однієї команди -> **STDIN** іншої
> - **STDERR** залишається на терміналі
> - Можна змінити потоки за допомогою спеціальних операторів

## Приклади

> [!example] Приклад
> ```bash
> echo $(systemctl list-units --type=target | grep custom | awk '{print $1 $2 $3}') $(systemctl list-dependencies custom.target | head -3 | sed s/[^a-z]//g | sort) | md5sum | cut -c 10-16
> ```


## Див. також

- [[перенаправлення потоків]]