---
date: 2025-07-04
title: Parameter expansion
draft: false
description: 
tags:
  - programming/bash
aliases:
  - bash parameter expansion
permalink: bash-parameter-expansion
lang: uk
---

> [!tldr]
> **Розширення параметрів** дозволяє маніпулювати та трансформувати значення [[Змінні у Bash|змінних]] під час їхнього використання.

## Синтаксис

```bash
"${paremeter:operator}"
```


## Значення за замовчуванням

- `${var:-default}` — `default`, якщо `var` пустий або не існує+
- `${var-default}` — `default`, якщо `var` не існує

## Присвоєння за замовчуванням

- `${var:=default}` —  присвоює `default`, якщо `var` пустий або не існує
- `${var=default}` — присвоює `default`, якщо `var` не існує

## Альтернативне значення

- `${var:+value}` — `value`, якщо `var` існує і не пустий
- `${var+value}` — `value`, якщо `var` існує

## Обробка помилок

- `${var:?error}` — виходить з помилкою `error`, якщо `var` пустий/не існує


## Операції з рядками

- `${#string}` — довжина рядка
- `${string:5}` — з 5-го символу до кінця
- `${string:5:3}` — з 5-го символу 3 символи
- `${string: -5}` — останні 5 символів (повинен стояти пробіл!!!)

## Заміна рядків

- `${string/old/new}` — перше входження old на new
- `${string//old/new}` — усі входження old на new
- `${string/#old/new}` — тільки на початку
- `${string/%old/new}` — тільки в кінці

## Видалення рядків

**Префікси (з початку)**:

- `${string#pattern}` — найкоротший префікс
- `${string##pattern}` — найдовший префікс

**Суфікси (з кінця):**

- `${string%pattern}` — найкоротший суфікс
- `${string%%pattern}` — найдовший суфікс

## Зміна регістру

- `${string^}` — перша літера у верхній регістр
- `${string^^}` — усі літери у верхній регістр

- `${string,}` — перша літера у нижній регістр
- `${string,,}` — усі літери

## Масиви

- `${array[@]}` — усі елементи
- `${#array[@]}` — к-сть елементів
- `${array[@]:2:3}` — 3 елементи починаючи з 2-го
- `${array[@]#pattern}` — видалити префікс для кожного



## Див. також

- [[Bash]]
- [[Змінні у Bash]]
- [[Масиви у bash]]
- [[Метасимволи bash]]

## Корисні джерела


- https://www.gnu.org/software/bash/manual/html_node/Shell-Parameter-Expansion.html