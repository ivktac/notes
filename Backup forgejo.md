---
created: 2025-08-15
title: Backup forgejo
tags:
  - backups
  - forgejo
publish: false
aliases: 
lang: uk
---
```bash
cd /var/backups
systemctl stop forgejo
tar cfz forgejo-$(date -I).tar.gz /var/containers/forgejo > /dev/null 2>&1
systemctl start forgejo
```