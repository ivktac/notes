---
date: 2025-07-04
title: Цикли у Bash
description: 
draft: 
tags:
  - programming/bash
aliases:
  - bash cycles
permalink: bash-cycles
lang: uk
---
# Цикли у bash

## Типи циклів

1. `for` — ітерація по списку

```bash
for file in *.txt; do
	echo $file
done
```

- `while` — виконання поки умова істина

```bash
while read line; do
	echo $line
done
```

- `until` — виконання поки умова хибна

```bash
counter=0
until [ $counter -qe 5 ]; do
	echo $counter
	((counter++))
done
```

- `select` — меню вибору

```bash
select option in "Hello" "Start" "Quit"; do
	case $option in
		"Hello") echo "Hello Bash" ;;
		"Start") echo "Starting script..." ;;
		"Quit") break ;;
		*) echo "Invalid option" ;;
	esac
done
```


## Керування циклами

- `break` — вийти з циклу
- `continue` — перейти до наступної ітерації


## Див. також

- [[Bash]]
- [[Масиви у bash]]
- [[Розгалуження у bash]]
- [[Логічні оператори у Bash]]