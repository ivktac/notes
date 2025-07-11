---
date: 2025-07-11
title: як перевірити чи працює mysql на хості
description: 
draft: false
tags:
  - 🦮how-to
  - databases/mysql
aliases: 
permalink: 
lang: uk
---

> [!example] Перевірити через сокет з'єднання
> ```bash
> ss -xap | grep mysql
> ```

> [!example] Перевірити з'єднання по мережі
> ```bash
> ss -na | grep 3306
> ```

## Див. також

- [[Основи роботи з MySQL]]