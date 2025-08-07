---
created: 2025-08-06
title: цикли у bash
tags:
  - bash
aliases:
  - cycles in bash
lang: uk
---

## Типи циклів

- `for` — ітерація по списку

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

