---
date: 2025-07-16
title: ніколи не використовуй git commit -m,  використовуй git commit -v
description: 
draft: false
tags:
  - programming/git
aliases: 
permalink: 
lang: uk
---

> [!warning] `git commit` відкриває редактор з зі змінними `$EDITOR` або з конфігурації гіта.

За допомогою `git commit -v` можна бачити різницю комітів ([[git diff]]) під час написання повідомлення коміту.

> [!question] Нащо?
> Щоб швидко перервірити правильність коміту та що саме змінено.

