2024-09-23 17:29
Status:
Tags:
___
# Updatedb Config File

The updatedb config file controls the beheviour of updatedb and can be controlled by the module in /etc/updatedb.conf.

This module contains these type of variables:

- `PRUNEFS=`any file indicated to this parameter will not be scanned by updatedb
- `PRUNENAMES=` space separated directories name that should not be scanned by updatedb.
- `PRUNEPATHS=` List of path name that should be ifnored by updatedb
- `PRUNE_BIND_MOUNTS=`boolean value, if this is yes should be directories mounteded elsewgere will be ignored.
___
## References
