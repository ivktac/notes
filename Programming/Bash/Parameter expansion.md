---
date: 2025-07-04
title: Parameter expansion
draft: 
description: 
tags:
  - programming/bash
aliases:
  - bash parameter expansion
permalink: bash-parameter-expansion
lang: uk
---

> [!tldr]
> **Parameter expansion** дозволяє маніпулювати та трансформувати [[Змінні у Bash|змінні]].

## Значення за замовчуванням

- `${parameter:-default}` — значення за замовчуванням
- `${parameter:=default}` — присвоює значення за замовчуванням (у змінну)
- `${parameter:+value}` — альтернативне значення
- `${parameter:?error}` — виводить помилку `error` у stderr

## Операції з рядками

- `${#var}` — вивести довжину рядка
- `${var:0:5}` — підрядок (від 0 до 5 символу)
- `${var/word/newword}` — замінити слово `word` на `newword`
- `${var//l/L}` — замінити усі входження l на L
- `${file##.*}` — видилити найкоротший префікс
- `${file##*/}` — видалити найдовший префікс
- `${file%.*}` — видалити найкоротший суфікс
- `${file%%/*}` — видилти найдовший суфікс

## Регістр

- `${var^}` — перша літера великою
- `${var^^}` — усі літери великі
- `${var,}` — перша літера маленькою
- `${var,,}` — усі літери маленькі

## Робота з масивами

- `${arr[@]#*a}` — видилати до першого 'a'
- `${arr[@]%*}` — видалити після останнього 'a'


> [!warning] Рідко використовується
> - `${!var}` — непряме посилання

## Див. також

- [[Bash]]
- [[Змінні у Bash]]
- [[Масиви у bash]]
- [[Метасимволи bash]]

## Корисні джерела


- https://www.gnu.org/software/bash/manual/html_node/Shell-Parameter-Expansion.html