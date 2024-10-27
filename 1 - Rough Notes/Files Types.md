2024-09-23 09:32
Status:
Tags:
___
# Files Types

The file type of a file is shown using ls -l the output of this command show all the information of the file like [[Access permissions]] too.

```bash
ls -l prova.txt 
-rw-r--r--  1 tommaso  staff  12 22 Set 16:55 prova.txt
```

The first letter of the utilities is: 
- - (normal file): can contain any data
- d (directory): special kind of file, contains information about other files and directoris
- l (symbolic link): pointer to a file

There are some other file type:
- d: They're physical or virtual device, usually disk like /dev/sda
- c: They're physical or virtual device, like bash 
- s: They're socket.

___
## References
