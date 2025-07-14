---
date: 2025-07-04
title: Директиви Apache
description: 
draft: 
tags:
  - web/apacahe
  - configuration
aliases:
  - apache directive
  - apache directives
permalink: apache-directives
lang: uk
---

> [!tldr]
> **Директива Apache** — це інструкція в конфігураційних файлах [[Apache HTTP Server|вебсервера Apache]], яка вказує серверу, як саме поводитись.

> [!info] Основні директиви
> - `ServerRoot "/etc/httpd"` — базовий шлях для відносних шляхів
> - `Listen 80` — порт для прослуховування, також можна вказати IP: `Listen 1.2.3.4:80`
> - `User apache`/`Group apache` — власник процесів обробки запитів
> - `ServerAdmin bird@flock.org` — email для повідомлень про помилки
> - `ServerName bird.paradise.com` — домене ім'я сервера
> - `DocumentRoot "/var/www/html"` — директорія з веб-контентом
> - `ErrorLog "logs/error_log"` — розташування журналу помилок
> - `LogLevel "warn"` — рівень деталізації журналу ("error", "notice", "debug")
> - `LogFormat` — [[LogFormat Apache|формат журналювання доступу]]

## Корисні джерела


- https://httpd.apache.org/docs/current/mod/quickreference.html