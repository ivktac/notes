---
created: 2025-08-16
title: Атрибути UDP
tags:
  - network
  - udp
aliases: 
lang: uk
---
UDP має специфічні атрибути, що робить його ідеальним для певних додатків.

1. **Transaction-oriented** для простого запиту-відповіді ([[DNS]], [[NTP]])
2. **Datagram-based** для моделювання інших [[мережеві протоколи|протоколів]] (IP tunneling, [[RPC]], [[NFS]])
- **Simple** для [[bootstraping]] ([[DHCP]], [[TFTP]])
- **Stateless** для великої к-сть клієнтів ([[IPTV]])
- **Low latency** для real-time додатків ([[VoIP]], [[RTSP]])
- **Multicast support** для [[broadcast]] ([[RIP]])