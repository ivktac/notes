---
created: 2025-08-06
title: how to convert seconds to hours minutes seconds in bash
tags:
  - bash
  - how-to
aliases: 
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

## Див. також

- [[date]]