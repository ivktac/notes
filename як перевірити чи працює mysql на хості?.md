---
created: 2025-08-06
title: як перевірити чи працює mysql на хості?
tags:
  - how-to
aliases: 
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