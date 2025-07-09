---
date: 2025-07-09
title: how to convert seconds to hours minutes seconds in bash
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
seconds=1000
date -d@"$seconds" -u +"%-H %-M %S"
```

Результат:

```
0 16 40
```