2024-09-22 16:46
Status:
Tags:
___
# Access permissions

The access permissions define exactly what:
- An user
- A group
- All
Could do with the file.
These permission can be queried and manipulated trough the utilities.

## Query information about a file permissions
`-l` option.
```bash
ls -l file.txt
```


# Query information about a directory
Using `-d` option.
```bash
ls -ld folder
```

# Permission of a file

The permission of a file are showned right after the [[Files Types]] as three groups of three character each, in the order of r, w and x. The - meaning lack of permission.

- **r**: Stands for read, and has an octal value of 4, they're related to reading the file.
- **w**: Stands for write and has an octal value of 2, they're related to editing on file.
- **x**: Stands for execute and has an octal value of 1, they're related to execute the file like scripts or executable.

# Permission on Directories
Similiar to file permission there's directory permission too:

- r: read files from the folder
- w: write file from the folder
- x: execute file from the folder

Let's take as example an edge case.
If we wanna execute a bin files from a directory where we have no read permission, we cannot do that. 

A quick view of information of the file.
![[Pasted image 20240923095141.png | 500]]
![[Screenshot 2024-09-23 alle 10.16.15.png]]
___
## References
