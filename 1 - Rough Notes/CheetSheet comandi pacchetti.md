---
tags:
  - chapter
type: 
weight:
---

2024-10-19 03:54
Status:
Tags:
___
# Cheetsheet comandi pacchetti

- [[APT source list]]
- [[APT source list Directory]]
- [[Yum]]

## Package manager locali

|                                         | Debian Package Manager                                  | Rpmi                  |
| --------------------------------------- | ------------------------------------------------------- | --------------------- |
| install                                 | dpkg -i pacchetto.deb                                   | rpmi -i pacchetto.rpm |
| elimina pacchetto                       | dpkg -r pacchetto                                       | rpm -e package        |
| eliminazione completa pacchetto         | dpkg -P pacchetto.deb                                   | x                     |
| lista pacchetti locali                  | dpkg -I or dpkg-query -l (nome opzionale) pacchetto.deb | rpm -qa package       |
| lista contenuto pacchetto               | dpkg -L (--files) pacchetto.deb                         | rpm -ql package       |
| search package                          | x                                                       | rpm -qip package      |
| Trova proprietario del file             | dpkg -S **path_file**                                   | rpm -qf file          |
| info pacchetto                          | dpkg --info path_pacchetto                              | rpm -qi package       |
| info pacchetto istallato                | dpkg -s pacchetto                                       | rpm -qip package      |
| Aggiorna index e metadati dei pacchetti | x                                                       |                       |
| Aggiorna effettivamente i pacchetti     |                                                         | rpm -U                |
| Lista repos                             |                                                         |                       |
| Aggiungere repo                         | x                                                       | x                     |
| Rimuovi repo                            |                                                         |                       |
| Enable e disable repository             |                                                         |                       |
| Enable e disable refresh repository     |                                                         |                       |


## Package manager repository

|                                         | APT SUITE                                            | APT | YUM                               | Zypper                               | DNF                             |
| --------------------------------------- | :--------------------------------------------------- | --- | --------------------------------- | ------------------------------------ | ------------------------------- |
| install                                 | apt-get install pacchetto.deb                        |     | yum install pacchetto.rpm         | zypper in package                    | dnf install package             |
| elimina pacchetto                       | apt-get remove pacchetto                             |     | yum remove package                | zypper rm package                    | dnf remove package              |
| eliminazione completa pacchetto         | apt-get purge pacchetto or apt-get --purge pacchetto |     | yum purge package                 |                                      | dnf purge package               |
| lista pacchetti locali                  | apt-cache                                            |     |                                   |                                      | dnf -l --installed              |
| lista contenuto pacchetto               | apt-file list file                                   |     | yum list package                  |                                      | dnf repoquery -l package        |
| search package                          | apt-cache search pacchetto                           |     | yum search package                | zypper se package                    | dnf search package              |
| Trova proprietario del file             | apt-file search file                                 |     | yum whatprovides file             | zypper se --provvides                | dnf provides package            |
| info pacchetto                          |                                                      |     | yum info package                  | zypper info package                  |                                 |
| info pacchetto istallato                | apt-cache show pacchetto.deb                         |     |                                   |                                      |                                 |
| Aggiorna index e metadati dei pacchetti | apt-get update                                       |     | yum update                        | zypper refresh                       |                                 |
| Aggiorna effettivamente i pacchetti     | apt-get upgrade                                      |     | yum upgrade                       |                                      |                                 |
| Lista repos                             |                                                      |     |                                   | zypper repos                         |                                 |
| Aggiungere repo                         | x                                                    |     | yum-config-manager add --add-repo | zypper addrepo                       | dnf config-manager-add_repo URL |
| Rimuovi repo                            |                                                      |     |                                   | zypper removerepo packman            |                                 |
| Enable e disable repository             |                                                      |     |                                   | zypper modifyrepo -d/-e repo-non-oss |                                 |
| Enable e disable refresh repository     |                                                      |     |                                   | zypper modifyrepo -f/-F repo-non-oss |                                 |
___
## References
[[LPIC-1 Exam 101.pdf#page=]]