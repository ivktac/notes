---
date: 2025-07-04
title: Розгалуження у bash
description: 
draft: 
tags:
  - programming/bash
aliases:
  - bash conditions
  - if statements bash
permalink: bash-conditions
lang: uk
---

##  Види розгалужень

- **if**
- **if-else**
- **if-elif-else**
- **case-statement**

## Приклади

- базовий if

```bash
if [ condition ]; then
  # код якщо умова істинна
fi
```

- if-else

```bash
if [ condition ]; then
  # якщо умова істина
else
  # якщо умова хибна
fi
```

- if-elif-else

```bash
if [ condition1 ]; then
  # якщо істина умова condition1
elif [ condition2 ]; then
  # якщо попердня умова хибна, а condition2 істина
else
  # якщо усі умови хибні
fi
```

- case-statemnt

```bash
case $variable in
	pattern1)
	   # відповідає умові pattern1
	   ;;
	pattern2|pattern3)
	  # відопвідає умові pattern2 або pattern3
	  ;;
	*)
	  # код за замовчуванням
	  ;;
esac
```

## Див. також

- [[Bash]]
- [[Логічні оператори у Bash]]
- [[Умовні оператори у Bash]]
- [[Цикли у bash]]