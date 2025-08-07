---
created: 2025-08-06
title: розділювач полів у bash
tags:
  - bash
aliases:
  - IFS
  - internal field separator
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
- [[Обробка ключів командного рядка у скриптах у bash]]
- [[Масиви у bash]]