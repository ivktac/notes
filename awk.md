---
date: 2025-07-05
title: awk
description: 
draft: 
tags:
  - man
  - programming/awk
  - os/text-processing
aliases: 
permalink: man-awk
lang: uk
---

> [!tldr]
> **awk** — повноцінна [[мова програмування]] та інструмент [[CLI|командного рядку]] для обробки та фільтрації структурованого тексту.

## Синтаксис

```bash
awk [опції] 'програма' [файл]...
awk [опції] -f скрипт [файл]...
```

## Основні змінні

- `$0` — весь поточний рядок
- `$1, $2, ..., $NF` — поля рядка (by default розділені пробілами)
- `NF` — кількість полів у рядку
- `NR` — номер поточного рядку
- `FS` — роздільник полів (за замовчування пробіл)

## Структура програми

```bash
awk 'BEGIN {ініціалізація} {обробка рядка} END {завершення}'
```

## Основні функції

- `print` — вивести рядок
- `printf` — форматований вивід
- `split(рядок, масив, роздільник)` — розділити рядок на масив

##  Умови та фільтри

- `$3 > 100` — числові умови
- `/^https/` — регулярні вирази
- `NR == 5` — номер рядка
- `$2 ~ /tcp/` — пошук по шаблону

## Секції

- `BEGIN` — виконується перед обробкою файлу
- `END` — виконується після обробки файлу
- Основна сексція — виконується для кожного рядка

## Приклади

- Вивести перше поле

```bash
awk '{print $1}' file
```

- Змінити роздільник

```bash
awk -F: '{print $1}' /etc/passwd
```

- Фільтрація з умовою

```bash
awk '$3 > 100 {print $1}' file
 ```

- Форматований вивід

```bash
awk '{printf "%-20s %s\n", $1, $2}' file
```

## Див. також

- [[Обробка тексту]]
- [[Регулярні вирази]]

## Корисні джерела

- https://www.baeldung.com/linux/awk-call-external-program
- https://www.howtogeek.com/562941/how-to-use-the-awk-command-on-linux/
- https://www.gnu.org/software/gawk/manual/html_node/Printf-Examples.html
- https://www.gnu.org/software/gawk/manual/gawk.html#Built_002din