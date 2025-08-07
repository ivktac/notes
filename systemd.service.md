---
created: 2025-08-06
title: systemd.service
tags:
  - systemd
aliases: 
lang: uk
---
## Сексція [Unit]

> [!note]-
> - **Description**: опис сервісу
> - **Documentation**: посилання на документацію
> - **After**: запускати після вказаних юнітів
> - **Before**: запускати перед вказаниими юнітами
> - **Requires**: жорстка залежність (якщо залежність падає, юніт також)
> - **Wants**: м'яка залежність
> - **Conflicts**: конфліктуючі юніти

```ini
[Unit]
Description=Опис сервісу
Documentation=https://example.com/docs
After=network.target syslog.target
Before=multi-user.target
Requires=network.target
Wants=syslog.target
Conflicts=shutdown.target
```

## Секція [Service]

```ini
[Service]
Type=simple
User=www-data
Group=www-data
WorkingDirectory=/var/www/myapp
Environment=NODE_ENV=production
EnvironmentFile=/etc/myapp/environment
ExecStart=/usr/bin/node server.js
ExecReload=/bin/kill -HUP $MAINPID
ExecStop=/bin/kill -TERM $MAINPID
PIDFile=/var/run/myapp.pid
Restart=on-failure
RestartSec=5
TimeoutStartSec=30
TimeoutStopSec=30
```

## Типи сервісів

| **Тип**   | **Опис**                                           |
| --------- | -------------------------------------------------- |
| `simple`  | процес не форкується (за замовчуванням)            |
| `exec`    | очікує завершення ExecStart                        |
| `forking` | процес форкується, батьківський завершується       |
| `oneshot` | виконується один раз, потім завершується           |
| `dbus`    | сервіс отримує ім'я на D-Bus                       |
| `notify`  | сервіс надсилає повідомлення через [[sd_notify()]] |
| `idle`    | затримка запуску до завершення інших задач         |

## Сексція [Install]

> [!note]-
> - **WantedBy**: в які targets включати при `enable`
> - **RequiredBy**: жорстка залежність для targets
> - **Also**: додатково вимкнути/увімкнути ці юніти
> - **DefaultInstance**: для template юнітів

```ini
[Install]
WantedBy=multi-user.target
RequiredBy=graphical.target
Also=myservice-helper.service
DefaultInstance=production
```

## Приклади

```ini
[Unit]
Description=Simple Web Server
After=network.target

[Service]
Type=simple
User=www-data
Group=www-data
WorkingDirectory=/var/www/html
ExecStart=/usr/bin/python3 -m http.server 8080
Restart=always
RestartSec=10

[Install]
WantedBy=multi-user.target
```

## Див. також

- [[systemd.target]]