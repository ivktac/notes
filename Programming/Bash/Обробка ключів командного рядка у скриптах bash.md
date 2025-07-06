---
date: 2025-07-04
title: Обробка ключів командного рядка у скриптах bash
draft: 
tags:
  - programming/bash
aliases:
  - bash keys script
description: 
permalink: bash-options-cli
lang: uk
---
##  Обробка ключів з [[getopts]]

```bash
while getopts "hf:v" opt; do
	case $opt in
	  h) echo "Help"; exit 0 ;;
	  f) filename="$OPTARG" ;;
	  v) verbose=true ;; 
	  \?) echo "Invalid key: -$OPTARG" >&2; exit 1 ;;
	esac
done
```

## Зсув до неопціональних аргументів

```bash
shift $((OPTIND-1))
```

##  Ручна обробка ключів

```bash
while [[ $# -gt 0 ]]; do
	case $1 in
		-f|--file) filename="$2"; shift 2 ;;
		-v|--verbose) verbose=true; shift ;;
		--help) echo "Help"; exit 0 ;;
		--) shift; break ;;
		-*) echo "Invalid key $1" >&2; exit 1 ;;
		*) break ;;
	esac
done
```

## Перевірка кількості аргументів

```bash
if [ $# -lt 1 ]; then
	echo "Usage: $0 <file>"
	exit 1
fi
```

## Див. також

- [[Позиційні параметри у bash|Позиційні параметри]]
- [[Parameter expansion]]