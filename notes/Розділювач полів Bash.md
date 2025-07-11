---
date: 2025-07-04
title: Розділювач полів Bash
description: 
draft: 
tags:
  - programming/bash
aliases:
  - internal field  separator
  - IFS
permalink: bash-internal-field-separator
lang: uk
---

> [!tldr]
> **IFS (Internal Fields Separator)** — [[Змінні у Bash|змінна]], яка визначає символи для розділення полів.

> [!tip] За замовчуванням: `^I$` (пробіл, табуляція, новий рядок)

## Приклади


> [!example] Приклад використання
> ```bash
> while IFS=":" read -r username hash uid gid gecos home shell; do
>   echo "$username: $home, ($shell)"
>  done < /etc/passwd
> ```

## Див. також


- [[Позиційні параметри у bash]]
- [[Обробка ключів командного рядка у скриптах bash]]
- [[Масиви у bash]]