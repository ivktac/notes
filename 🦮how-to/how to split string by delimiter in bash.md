---
date: 2025-07-09
title: how to split by comma and loop it in bash
description: 
draft: false
tags:
  - 🦮how-to
  - programming/bash
aliases: 
permalink: 
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