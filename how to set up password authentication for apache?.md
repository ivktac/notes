---
created: 2025-08-06
title: how to set up password authentication for apache?
tags:
  - how-to
  - apache
aliases: 
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

## Див. також

- [[Apache HTTP Server]]