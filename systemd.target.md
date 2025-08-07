---
created: 2025-08-06
title: systemd.target
tags:
  - systemd
aliases: 
lang: uk
---

## Навіщо?

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