2024-09-23 14:56
Status:
Tags:
___
# sticky bit

The sticky is a permission part of [[Special Permissions]].
And it is used for indicate the authorization for deleting directories.
If the sticky bit is setted if you are not the owner or the administrator you cannot delete and rename files from this folder.

When the sticky bit is setted on you can see him in symbolic mode like:

```bash
--w-rw-rwT  1 tommaso  staff   0 23 Set 14:48 lol
```
There's a T at the ending of the file.
It's the last bit of the authorization bits.
In octal reppresentation is 1.
___
## References
