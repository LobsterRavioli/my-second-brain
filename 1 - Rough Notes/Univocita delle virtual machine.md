---
tags:
  - chapter
type: 
weight:
---

2024-10-19 07:07
Status:
Tags:
___
# Univocita delle virtual machine

- MAC address

- Chiavi ssh
```bash
ssh-keygen -A # Aggiorna le chiavi private
ssh-copy-id -i <chiave pubblica> user@cloud_server   #aggiorna anche le chiavi pubbliche a chi le ha
```
- D-Bus ID
dbus-uuidgen --ensure
```bash
dbus-uuidgen --ensure   #vedi se esiste
dbus-uuidgen --get # fatti dare l'id della vm
```

```bash
sudo rm -f /etc/machine-id    #rimuovilo
sudo dbus-uuidgen --ensure=/etc/machine-id   #generalo
```
sudo rm -f /etc/machine-id
$ sudo rm -f /etc/machine-id $ sudo dbus-uuidgen --ensure=/etc/machine-id

___
## References
[[LPIC-1 Exam 101.pdf#page=]]