---
created: 2025-08-08
title: Види шаблонів у awk
tags:
  - awk
  - scripting
aliases:
  - types of patterns in awk
lang: uk
---
- `BEGIN { statements }` — виконується один раз перед читанням вводу
- `END { statements }` — виконується один раз після прочитання усіх рядків
- `expression { statements }` — виконується для кожного рядку, якщо `expression` є `True` (nonzero або nonnull)
- `/regular expression/ { statements }` — виконується для кожного рядку, що відповідає регялурному виразу
- `compound pattern { statements }` — кобмінація логічних операцій `&&` (AND), `||` (OR), `|` (NOT)  та дужок, виконується коли `True`
- `pattern1, pattern2 { statements }` — діапазон шаблонів, виконується для кожного рядку, який відповідає `pattern1` до наступного збігу з `pattern2` (включно)

## Див. також

- [[Логічні оператори у awk]]
- [[Шаблони рядкових збігів у awk]]