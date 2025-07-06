---
date: 2025-07-04
title: Масиви у bash
description: 
draft: 
tags:
  - programming/bash
aliases:
  - bash arrays
permalink: bash-arrays
lang: uk
---

> [!tldr]
> **Масиви** в [[Bash]] дозволяють зберігати кілька значень в одній змінній.

## Типи масивів

1. **Індексні** масиви (з числовими індексами)

```bash
numbers=(1 2 3 4 5)
fruits=("apple" "banana" "orange")
```

2. **Асоціативні** масиви ("ключ-значеня")

```bash
declare -A data
data["username"] = "gearxxed"
data["age"] = "23"
data["city"] = "Chernivtsi"
```

## Доступ до елементів

- По індексу або ключу
```bash
echo ${fruits[0]}
echo ${data["username"]}
```

- Усі елементи

```bash
echo ${fruits[@]}
echo ${fruits[*]}
```

- Вивести тільки індекси (для асоціавтиних виведе ключі)

```bash
echo ${!fruits[@]}
echo ${!data[@]}
```

- Вивести кількість елементів

```bash
echo ${#fruits[@]}
```

## Операції з масивами

- Додати елемент

```bash
fruits+=("grape")
```

- Видалити елемент 

```bash
unset fruits[1]
# видалити весь масив
unset fruits
```

- Отримати зріз масиву

```bash
# починаючи з індексу 1, 2 елементи
echo ${fruits[@]:1:2} 
```

- Замінити у масиві

```bash
echo ${fruits[@]/apple/pear}
```

## Ітерація по масивах

- По значеннях

```bash
for fruit in "${fruits[@]}"; do
	echo $fruit
done
```

- По індексах

```bash
for i in "${!fruits[@]}"; do
	echo "$i — ${fruits[i]}"
done
```

- По ключам (асоціативний масив)

```bash
for key in "${!person[@]}"; do
	echo "$key: ${person["key"]}"
done
```

## Див. також

- [[Змінні у Bash]]
- [[Цикли у bash]]
- [[Parameter expansion]]