---
date: 2025-07-14
title: Ansible templates
description: 
draft: false
tags:
  - devops/ansible
aliases: 
permalink: 
lang: uk
---

**Шаблони** у [[Ansible]] використовують [[Jinja2]] для динамічного створення конфігураційних файлів. Це дозволяє підставляти змінні в шаблони.

> [!example]
> ```xml
><VirtualHost *:{{ apache_port }}>
>    ServerName {{ server_name }}
>    DocumentRoot {{ document_root }}
> </VirtualHost>
>```