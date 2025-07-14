---
date: 2025-07-14
title: як встановити аутентифікацію у apache?
description: 
draft: false
tags:
  - 🦮how-to
  - web/apacahe
aliases: 
permalink: 
lang: uk
---
```bash
htpassswd -cb /etc/httpd/.htpasswd "$HTTPD_USER" "$HTTPD_PASSS"
```

у httpd.conf:

```yaml
AuthType Basic
AuthName "Resitrcted Content"
AuthUserFile "/etc/httpd/.htpasswd"
Require valid-user
```