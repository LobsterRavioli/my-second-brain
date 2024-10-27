# lspic

lspci -v
lspci -s (filter for slot ID)
lspci -k (moduli kernel)


# lsusb
lsusb -s (filter for slot ID)
lsusb -d (filter for id ID)
lsusb -t (tree vision)


# lsmod

lsmod (show kernel modules statsu)
# modprob

modprob -r snd-hda-intel (remove kernel module)

# modinfo
modinfo -p modulo_kernel  (mostra i parametri per il modulo kernel)


# lsusb
lsusb (device usb attualmente collegati)


# Fase di avvio del Bios
- Bios check dei filesystem
- Bios attiva l'hardware input e output
- Bios carica bootloader da MBR e quindi dai primi 440 bytes del disco (512 sono dedicati a MBR e 440 sono dedicati ai file di avvio questi sono posizionati nel primo disco e nella prima partizione)
- Il primo stage del bootloader carica il secondo stage del bootloader responsabile nella visione del menu ecc

# Fase di avvio di UEFI
- UEFI check dei filesystem
- UEFI attiva l'hardware input e output
- UEFI carica la standard uefi application che sarebbe il bootloader dalla NVRAM situata dalla EFI system partition.
- il primo stage chiama il secondo.


# Parametri del kernel di grub

- acpi (supporto acpi)
- init (imposta il processo da eseguire appena il bootloader carica il kernel, puo essere un init o bash)
- mem (importa la ram massima per il sistma)
- maxcpu (imposta i core del processore)
- quiet (silenzia i messaggi di boot)
- vga (seleziona la modalita video)
- root=/dev/sda3(seleziona la partizione di root)
- rootflags (opzioni di mount per la root filesystem)
- ro (rendi la mount iniziale della root in  modalita readonly)
- rw (rendi la modalita della root in scrittura e lettura)

I parametri devono essere aggiunti nel /etc/default/grub nel campo GRUB_CMDLINE_LINUX per renderli persistenti e poi si genera il relativo file di configurazione con grub-mkconfig


# dmesg
dmesg (mostra il kernel ring buffer contentene i log del kernel e del boot)

# journalctl

- journalctl 
- journalctl -b
- jornalctl --list-boots (mostra tutti i boots)
- journalctl -b 0 (mostra i log relativi all'ultimo boot)
- journalctl -b -1 (mostra i log relativi al boot precedente)


# Runlevels di Sysvinit
- 0 shutdown
- 1: single user mode no network
- 2: multi user mode senza network solo terminale
- 3: muti ser mode con network e terminale
- 4: modalita personalizzata
- 5 multiuser mode con GUI e quindi interfaccia utente e desktop grafico
- 6: restart


# Struttura inittab
id:runlevels:action:process
- id a cas
- runlevel: runlevel di riferimento (da 0 a 6)
- action 
	- boot: eseguito in fase di inizializzazione
	- bootwait: init aspettera che il processo completi in fase di inizializzazione
	- sysinit: dopo la fase di iniizializzazione
	- wait: init aspettera quando finira/
	- respawn: se verra terminato sara rieseguito
	- ctrlaltdel: il processo verra eseguito con ctrl+alt+del


# telinit

telinit runlevel (starta  il runlevel)
telinit 0 (spegni)
telinit 6 (riavvia)

# runlevel
runlevel (printa il runlevel)

# resize2fs

resize2fs 

# mkfs

# mkswap
mkswap

# swapon
swapon

# swapoff
swapoff

# du
df (usage of the current directory)
du -h (human readable)
du -ah (all, disk usage of all files not only directories)
du -Sah (disk usage )
du -ah --exclude="*.bin"

# df
df (disk free of filesystem)
df -h (human readable)
df -i (inodes)
df -hT (show filesystem type too)
df -hx ext4 (exclude ext4 filesystems)
df -ht ext4 (filter for ext4 filesystems)
df -o=target,source,fstype, pcent (forma output for target, source, fstype and pcent)

--ouput could be:
- itotal
- iused
- iavail
- ipcent


# fsck

fsck -A (check all fstab)
fsck -C (progress bar)
fsck -N (simulate the fsck)
fsck -R (skip root filesystem)
fsck -V (verbose mode)

# enfck2
e2fsck (working for ex2, ext3 and ext4)
e2fsck -p (automatically fix all errors)
e2fsck -n (simulate e2fsck)
e2fsck -f (force e2fsck)


# tune2fs

tune2fs -l /dev/sda1 (list filesystem parameter)
tune2fs -c 1 (set counter of fsck)
tune2fs -C 10 (set value of the counter of fsck)
tune2fs -i (set interval for checks)
tune2fs -e (set beheviour)
tune2fs -j (add a journaling system)


# xfs_repair
xfs_repair -n /dev/sdb1  (simulate the repair)
xfs_repair -m /dev/sdb1 (set memory usage)
xfs_repair -d (dangerous mode repair read only filesystems)
xfs_repair -v (verbose mode)


# xfs_db
xfs_db  /dev/sdb1  (inspect the parameter of xfs filesystem)



# mount
mount (list current mounted filesystem)
mount -t (list current mounted filesystem of type t)
mount -t ext4 partition mountpoint
mount -t ext4 UIID mountpoint

mount -a (mount all fstab filesystem)
mount -o (define optional options like fstab)
mount -r (read only)
mount -rw (read and write)

# lsof
ldof /dev/vda1 (show current processes working on vda1 partition)

# lsblk
lsblk -f /dev/vda1 (show UUID of vda1 partition)



# touch
touch -am
# find
find -type d
find -type f
find -type l
find -iname
find -maxdepth N
find -mtime
find . -name "*.conf" -exec chmod 644 '{}' \;
find -size
find -user
find -group
find -readable
find -executable
find -perm
find -empy
find -size N
find -amin N (file che sono stati aperti N minuti fa)
find -cmin N (file i cui attributi sono stati modificati N minuti fa)
find -mmin N (file che sono modificati aperti N minuti fa)
find -atime N (file che sono stati aperti Nx24 fa)
find -ctime N (file i cui attributi sono stati modificati Nx24 minuti fa)
find -mtime N (file che sono modificati aperti Nx24 minuti fa)

# tar
tar -c (create)
tar -x (extract)
tar -t (test)
tar -v  # (verbose)
tar -f  # (specifica nome file)
tar -j  # (bunzip2)
tar -z  # (gzip)

# cpio
cpio -o  # (output)
cpio -i  # (estrazione)
cpio -id nome_directory  # (estrazione e crea directory)

# uniq
uniq -c  # (conta occorrenze di una linea per ogni linea)

# uname
uname -o  # (OS)

# jobs
jobs -l  
jobs -n  
jobs -p  # (pid)
jobs -r  # (jobs in esecuzione)
jobs -s  # (jobs sospesi)
jobs -n  # (jobs che hanno cambiato stato recentemente)

# nohup
nohup  # (scollega dalla sessione)

# watch
watch
watch -n  # (intervallo di aggiornamento in secondi)

# top
top
- M  # (memory)
- T  # (execution time)
- N  # (per pid number)
- P  # (percentage CPU time)
- k  # (kill a process)
- r  # (renice)
- u  # (user process)
- c  # (path assoluti)

# nice
nice -n 10  # (imposta valore nice)
renice -x  # (x sta per valore di nice)
renice -p 8123  # (indica il pid)

# grep
grep -c  # (count)
grep -i  # (ignore case)
grep -f  # (file con le regex)
grep -n  # (mostra numero di riga)
grep -v  # (inverted match)
grep -H  # (print nome file)
grep -z  # (usato con -print0 di find)

# sed
sed 1,7d  # (eliminazione di righe)
sed "/lol/d"  # (eliminazione con match)
sed "1,7d;/lol/d"  # (concatenazione di comandi)
sed "/lol/ c REMOVED"  # (sostituzione riga con REMOVED)
sed "s/stringa1/stringa2/g"  # (sostituzione)
sed -e 's/.* \(stringa1\)$/\1/'  # (cattura stringa1 nel campo 1 con sostituzione)

# mkfs
mkfs -t  # (scegli il tipo)
mkfs -t  # (check for bad blocks)
mkfs -d  # (indica la cartella che andrà nella root del filesystem)
mkfs -F  # (forza la creazione del filesystem)
mkfs -L  # (imposta etichetta del volume)
mkfs -n  # (simula il montaggio)
mkfs -q  # (silenzia l'output)
mkfs -V  # (verbose output)
mkfs -U UID  # (imposta UUID per il filesystem)

# mkfs specifico
mkfs.xfs
mkfs.exfat
mkfs.btrfs

# btrfs
btrfs subvolume create
btrfs subvolume show
btrfs subvolume snapshot

# parted
parted
- print
- print free
- print devices
- mklabel gpt
- mklabel msdos
- rescue
- resize part
- mkpart primary linux-swap begin end

# swap
mkswap  
swapon
swapoff

# resize
resize2fs

# du (disk usage)
du  # (disk usage della cartella attuale)
du -a  # (mostra conteggio file per tutti)
du -S  # (esclude le sottocartelle)
du -h  # (human readable)
du -c  # (aggiungi il totale a fine conteggio)
du -d1  # (specifica la profondità)
du --exclude=path_directory  

# df (disk free)
df  # (spazio libero da ogni filesystem montato)
df -h  # (human readable)
df -i  # (inodes)
df -t ext2  # (filtra per tipo di filesystem)
df -T  # (stampa anche il tipo di filesystem)
df -ix xtfs  # (escludi il tipo di filesystem)
df --output=target,source,fstype,pcent

# fsck (filesystem check di filesystem non montati)
fsck -A  # (controlla tutti i filesystem in fstab)
fsck -C  # (visualizza barra progresso)
fsck -N  # (simula il check)
fsck -R  # (skippa il root)
fsck -V  # (verbose)
fsck -t ext2  # (specifica il filesystem)

# e2fsck
e2fsck /dev/sda1  # (filesystem check su ext2/3/4 non montati)
e2fsck -p  # (correggi automaticamente)
e2fsck -y  # (sì a tutte le domande interattive)
e2fsck -n  # (no a tutte le domande interattive)
e2fsck -f  # (forza il check)

# tune2fs
tune2fs -l /dev/sda1
tune2fs -c 10  # (controllo fsck dopo 10 montaggi)
tune2fs -C 10  # (imposta il contatore dei montaggi a 10)
tune2fs -i 10d  # (controllo fsck ogni 10 giorni)
tune2fs -e {panic,continue,remount-ro}  # (comportamento in caso di errori del filesystem)
tune2fs -j /dev/sda1  # (aggiungi un journal - diventa ext3)
tune2fs -J size=10,location=100M,device=/dev/sdb1  # (journal personalizzato)

# xfs_repair
xfs_repair -n /dev/sda1  # (simula il check del filesystem XFS)
xfs_repair -l dispositivo -r dispositivo  # (necessari per il funzionamento del filesystem)
xfs_repair -d  # (modalità dangerous, abilita la riparazione dei dispositivi montati in sola lettura)
xfs_repair -m N  # (limita l'utilizzo della memoria a N megabyte)

# xfsdb
xfsdb  # (debugging interattivo come parted)

# dump2fs
# mount
mount -t ext2 partition target  # (monta la partizione nella cartella target)
mount -t ext2  # (elenca tutti i filesystem montati di tipo ext2)
mount -o options  # (opzioni di fstab per il remount)
mount -ro partition target  # (monta in sola lettura)
mount -w  # (monta il filesystem in scrittura)

# umount
umount -a  # (smonta tutti i filesystem di fstab)
umount -f  # (forza lo smontaggio)
umount -r  # (se non può essere smontato, montalo in sola lettura)

# lsof
lsof  # (mostra i processi che impediscono lo smontaggio del filesystem)

# fstab
FILESYSTEM MOUNTPOINT TYPE OPTIONS DUMP PASS
FILESYSTEM: dispositivo da montare o UUID
MOUNTPOINT: cartella dove montare
type: tipo di filesystem da montare
Parametri:
Dump: esegui comando dump per il filesystem
Pass: ordine di controllo del filesystem
# parametri fstab
- atime / noatime  # (indica l'aggiornamento di accesso per ogni file letto)
- auto  # (il filesystem può essere montato con mount -a)
- dev  # (interpreta il dispositivo a blocchi)
- mode  # (interpreta il dispositivo a caratteri)
- exec  # (consente esecuzione di file binari)
- noexec  # (non consente l'esecuzione di file binari)
- user: allow an a non root user to moutn the filsystem
- nouser: do not allow a non root user to mount a filesystem
- suid: allor setup setguid and setgid
- ro: mount a filesystem in read only
- rw: mount a filesystem in write only
- remount: flag per mount -o per rimontare il filesystem.
- sync: operazioni input e output in maniera sincrona.
- async: operazioni input e output in maniera asincrona.

# lsblk

lsblk (Mostra tutti i file system  presenti sul sistema)
lsblk -f /dev/sda1 (Mostra l'UUID del filesystem e la label)

# Montaggio systemd

E' possibile sostituire fstab con systemd.

/etc/systemd/system/medio-disco.mount

\[Unit\]
Description=Montaggio della partiione sdb

\[Mount\]
What=/dev/disk/by-uuid/UUID
Where=/media/cartella
Type=ext4
Options=defaults
\[Install\]

systemctl daemon-reload
systemctl start mnt-unit.mount
systemctl enable mnt-unit.mount

# ls
ls -l (permessi,contatore hard links, utente, gruppo, grandezza, timestamp, nome cartella)
![[Screenshot 2024-10-22 alle 11.25.09.png|300]]

# chmod

- Notazione ottale 
chmod 0666 file.txt

- Notazione simbolica
chmod x=rwx, g=rwx, o=rwx file
chmod x+rw, g

- Notazione simbolica abbreviata
chmod ugo+wrx


# gtent, groups, groupsmem

list the groups on your system


# umask

I file di default hanno bit 666.
Le directory 777.
- read per le directory equivale al listing della directory
- write alla creazione e modifica dei file
- execute alla apertura
umask 666
umask u=rwx,g=rwx,o=rwx



# ln

- Link simbolico
ln -s file.txt symbolic_link.txt

- Hard likn
ln file.txt hard_link.txt


# Locate

locate .jpg
locate -i .jpg (ignore case)
locate -A .jpg .zip (matcha tutti i pattern forniti)
locate -c .jpg (Conteggio dei match)


# wich
which binary_file (show path from $PATH)
which -a binary_file (show all paths from $PATH)
# type
type command (show type of file and path)
type -t command (show the type {file, built-in, keyword, function} of a command )
type command -a (show type of file and every path)

# whereis
whereis command (show path and source code)
whereis -b command (show path of binary)
whereis -s command (show path for source code)
whereis -m command (show path for the man page)



