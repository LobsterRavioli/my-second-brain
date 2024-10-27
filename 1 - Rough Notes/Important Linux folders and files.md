2024-09-25 07:27
Status:
Tags:
___
# Important Linux Folders and files

- [[Filesystem Hierarchy Standard]]
- [[Storage folders]]
- [[fstab]]
- [[inittab]]
- [[Location Temporary Files]]
-  [[updatedb.conf]]


| path                    | description                                                                                   |
| ----------------------- | --------------------------------------------------------------------------------------------- |
| proc/cpuinfo            | Lists detailed information about the CPU(s) found by the operating system.                    |
| /proc/interrupts        | Contiene le info relative agli interrupts dei processori                                      |
| /proc/ioports           | Contiene tutte le porte input output.                                                         |
| /proc/dma               | contiene le posizioni sulla memoria dei dispositivi                                           |
| /etc/udev/rules.d       | Contiene moduli che definiscono le regole di udev (il gestore dei dispositivi)                |
| /etc/fstab              | Contiene le indicazioni per il montaggio dei device                                           |
| /var/log/               | Folder that contains system log                                                               |
| /sbin/init              | Binary for init file                                                                          |
| /etc/inittab            | contiene gli scripts da eseguire associati ai run levels da SysVinit                          |
| /etc/init.d/            | gli scripts da init indicati da initab                                                        |
| /etc/init               | Folder that contains initliazation scripts for Upstart                                        |
| /lib/systemd/system     | Contiene le unita di systemd di sistema (non modificabili)                                    |
| /etc/systemd/system/    | Contiene le unita configurabili per systemd                                                   |
| /etc/grub.d             | contiene gli script che rappresentano le entry per grub.cfg e l'ordine di quest'ultimi.       |
| /etc/grub/boot/menu.lst | Configurazione di menu di grub                                                                |
| /proc/cmdline           | Parametri del kernel attuali                                                                  |
| /etc/apt/sourcelist.d   |                                                                                               |
| /etc/yum.repos.d/       |                                                                                               |
| /etc/systemd/system     | Cartella contenente le unita .mount e .service                                                |
| /etc/modprobe.d/        | Cartella contenente file di configurazione file .conf per parametri custom dei moduli kernel. |
| /proc/dma               |                                                                                               |
| /proc/cpuinfo           |                                                                                               |
| /proc/ioports           | porte input e output in uso                                                                   |
| /proc/interrupts        | quanti interrupts input e output riceve la cpu                                                |
| /etc/udev.rules.d       | Contains rules of udev for detecting folder of devices                                        |
| /dev/hda, /dev/hdc      | Dischi rigidi primari con interfaccia IDE/PATA                                                |
| /dev/hdb,/dev/hdd       | Dischi rigidi slave con interfaccia IDE/PATA                                                  |
| /dev/hdb2               | Partizioni primarie o estese                                                                  |
| /dev/hdb5 - /dev/hdb12  | Partizioni logiche da 5 a 12                                                                  |
| /dev/sda,sdb,sdc        | Dischi SCSI,SATA o USB                                                                        |
| /dev/sdx1               |                                                                                               |
| /dev/mmcblk0            | Cartella che identifica la Microsd                                                            |
| /dev/mmcblk0p1          | Cartella che identifica la partizione della microsd                                           |
| /var/log                | Cartella contenente tutti i log del sistema                                                   |
| /var/log/journal/       | Cartella contente tutti i log di journalctl                                                   |
| /sbin/init              | Programma init di avvio che inizializza il sistema e definisce i runlevels                    |
| /etc/init.d             | Contiene gli script di esecuzione utilizzati da Systemv (service file)                        |
|                         | rc 0, rc 1, rc 2 associato ad ogni run level.                                                 |


| `/lib/systemd/system` | Systemd units started from systemd.                                        |
| --------------------- | -------------------------------------------------------------------------- |
| `/dev/udev/rules.d`   |                                                                            |
| `/lib/systemd/system` | Systemd units started from systemd.                                        |
| `/etc/init.d`         | Configuration files of system start                                        |


___
## References
