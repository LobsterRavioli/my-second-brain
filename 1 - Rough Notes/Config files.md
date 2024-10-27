2024-09-25 07:27
Status:
Tags:
___
# Config files

- [[GRUB|Kernel Grub Parameters]]
- [[fstab|Fstab Parameters]]


| /etc/init.d/                           |                                                                                       |
| -------------------------------------- | ------------------------------------------------------------------------------------- |
| /etc/systemd/                          |                                                                                       |
| /usr/lib/systemd/                      |                                                                                       |
| `/etc/inittab`                         | Configurazione dei runlevel (SysV init).                                              |
| **File**                               | **Descrizione**                                                                       |
| **/etc/systemd/system/default.target** |                                                                                       |
| **/etc/modprov.d/blacklist**           | Disabilita il modulo kernel al lancio                                                 |
| **/etc/systemd/system.conf**           | Configuration file of systemd                                                         |
| **/etc/init**                          | Configuration files of system start                                                   |
| **/dev/udev/rules.d**                  |                                                                                       |
| **grub.conf**                          |                                                                                       |
| **/boot/grub/grub.cfg**                | File generato da update-grub                                                          |
| **menu.lst**                           |                                                                                       |
| **/etc/default/grub**                  | File di configurazione modificabile con vari parametri e aggiornabile con update-grub |
| **/etc/apt/sources.list**              | File di configurazione per le repository di apt                                       |
| **/etc/yum.conf**                      | File di configurazione di yum dove è possibile specificare le repository              |
| **/etc/mtab**                          | Elenca i filesystem attualmente montati (generato dal sistema).                       |
| **.bash_history**                      |                                                                                       |
| **/etc/updatedb.conf**                 | File di configurazione per updatedb                                                   |
| **/etc/init.d/**                       |                                                                                       |
| **/etc/systemd/**                      |                                                                                       |
| **/usr/lib/systemd/**                  |                                                                                       |
| **/etc/inittab**                       | Configurazione dei runlevel (SysV init).                                              |
| /etc/modprob.conf                      | File dove vengono definiti parametri custom su kernel                                 |
| /etc/inittab                           | File dove vengono definiti gli scripts da eseguire definiti nella cartella init.d     |




___

## References
