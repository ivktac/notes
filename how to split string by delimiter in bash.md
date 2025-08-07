---
created: 2025-08-06
title: how to split string by delimiter in bash
tags:
  - how-to
  - bash
aliases: 
lang: uk
---

```bash
for item in ${string//,/}; do
	echo "$item"
done
```

Або

```bash
IFS=',' read -ra ARRAY <<< "$string"
for item in "${ARRAY[@]}"; do
	echo "$item"
done
```

## Див. також

- [[розширення параметрів у bash|parameter expansion in bash]]