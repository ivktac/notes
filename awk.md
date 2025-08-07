---
created: 2025-08-06
title: awk
tags:
  - cli
  - text-processing
  - awk
aliases: 
lang: uk
---
> [!tldr]
> `awk` — повноцінна [[мова програмування]] та інструмент [[cli|командного рядка]] для обробки та фільтрації структурованого тексту.

```bash
awk 'program' input files # код як рядок
awk -f profile input files # код як файл
some_command | awk 'program' # код як рядок
```

> [!note]
> Також можна використовувати [[шебанг]] для [[сценарії оболонки|скриптів]]:
> ```awk
> #!/usr/bin/env awk -f
> BEGIN { print "Hello, world!" }
> ```

## Див. також

- [[Стуктура програми awk]]
- [[Обробка тексту]]
- [[регулярні вирази]] 

## Корисні джерела

- https://www.baeldung.com/linux/awk-call-external-program
- https://www.howtogeek.com/562941/how-to-use-the-awk-command-on-linux/
- https://www.gnu.org/software/gawk/manual/html_node/Printf-Examples.html
- https://www.gnu.org/software/gawk/manual/gawk.html#Built_002din