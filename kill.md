---
date: 2025-07-10
title: kill
description: 
draft: false
tags:
  - os/process
  - man/kill
aliases: 
permalink: 
lang: uk
---

> [!tldr]
> **kill** —  команда для надсилання [[сигнали процесів|cигналу]] процесу.

## Синтаксис

```bash
kill [-s ім'я сигналу|-ім'я сигналу | -номер_сигналу] pid ...
```

> [!example] Примусово завершити процес
> ```bash
> kill -9 5070 # або kill -KILL 5070
> ```

> [!warning] Важливо
> Якщо не вказати, сигнал за замовчуванням надсилатиметься `TERM (15)`.

> [!tip] `kill -l` - щоб отримати список усіх доступних сигналів.

## Див. також

- [[killall]]