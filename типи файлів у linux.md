---
date: 2025-07-03
title: Типи файлів у Linux
description: 
draft: 
tags:
  - os/🐧linux
  - os/filesystem
aliases:
  - type files in linux
permalink: type-files-in-linux
lang: uk
---

[[Linux]] розрізняє 7 основних типів файлів, кожен з яких має своє призначення:

| **Символ** | **Тип**                                    | **Пояснення**                                                                             | **Приклад**                 |
| ---------- | ------------------------------------------ | ----------------------------------------------------------------------------------------- | --------------------------- |
| `-`        | [[файл\|Звичайний файл]] (regular)         | Файл, що містить корисні дані і безпосередньо використовується. Не є спеціальним як інші. | `text.txt`, `picture.jpg`   |
| `d`        | [[Каталог]] (directory)                    | Файл, який зберігає імена файлів та їхні inode.                                           | `~/Documents`               |
| `s`        | [[symlink\|Символьне посилання]] (symlink) | Посилання на інший файл                                                                   | `/bin -> usr/bin`           |
| `b`        | Блочний пристрій (block device)            | Пристрій, який передає дані блоки фіксованого розміру                                     | `/dev/sda1`                 |
| `c`        | Символьний пристрій (character device)     | Пристрій, який перадає дані посимвольно                                                   | `/dev/tty`                  |
| `p`        | Канал ([[pipes]])                          | Одностороння міжпроцесорна взаємодія                                                      | `gxx_admin@gearxxed.com:22` |
| `s`        | [[Сокет]] (socket)                         | Двостороння міжпроцесорна взаємодія                                                       | у bash: \|                  |
## Див. також

- [[Метадані файлу (inode)]]
- [[file]]
- [[як визначити тип файлу?]]
- [[як показати тільки каталоги?]]