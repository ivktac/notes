---
date: 2025-07-13
title: деякі корисні аліаси bash
description: 
draft: false
tags:
  - programming/bash
  - man/bash
  - os/cli
aliases: 
permalink: 
lang: uk
---

## Багаторівневий `..`

```bash
up() { cd "$(eval printf '../'%0.s "{1..$1}")" || return 1; }
```

## Швидко перейти у тимчасову створену директорію

```bash
cdtmp() { cd "$(mktemp -d)" || exit; }
```

## Linux cheats

```bash
cheat() { curl "cheat.sh/$1"; }
```

## Див. також

- [[Bash]]
- [[alias]]