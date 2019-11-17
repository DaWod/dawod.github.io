---
layout: post
title:  "Arch Linux - Configuration Tipps"
---

# DHCP
* Mit ip link kann die Netzwerkkarte bestimmt werden
* Installation des DHCP-Service: pacman -S dhcpcd
* Ob ich das hier noch machen muss, weiß ich nicht mehr: nano /etc/systemd/network/enp0s3.network
* Dort das hier eintragen: 
```
[Match] 
name=en* 
[Network] 
DHCP=yes
```
* systemctl enable dhcpcd@enp0s3 -> Nach Reboot automatisch starten
* systemctl start dhcpcd@enp0s3 -> jetzt starten
* ping funktioniert
