---
created: 2025-08-08
title: Шаблони рядкових збігів у awk
tags:
  - awk
  - scripting
aliases: 
lang: uk
---
- `/regexpr/` (те саме, що `$0 ~`) — перевіряє збіг у рядках, які містять підрядок `regexpr`
- `expression ~ /regexpr/` — збіг, якщо рядок `expression` містить підрядок `regexpr`
- `expression !~ /regexpr/` — збіг, якщо рядок `expression` не містить підрядок `regexpr`

> [!warning] Будь-який вираз, може використовуватися на місці `/regexpr/` у контексті `~`  та `!~`.
