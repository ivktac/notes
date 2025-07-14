---
date: 2025-07-07
title: systemd.target
description: 
draft: false
tags:
  - man/systemd/target
aliases:
  - systemd targets
  - таргети сістемд
permalink: man-systemd-target
lang: uk
---

## Для чого?

- Групування [[Типи юнітів у systemd|юнітів]]
- Визначення станів системи
- Синхронізація запуску

## Приклад

```ini
[Unit]
Description=Multi-User System
Documentation=man:systemd.special(7)
Requires=basic.target
Conflicts=rescue.service rescue.target
After=basic.target rescue.service rescue.target
AllowIsolate=yes
```

## Див. також

- [[systemd.service]]