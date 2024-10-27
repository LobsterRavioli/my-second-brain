2024-09-22 15:53
Status:
Tags:
___
# Systemd auto-mount unit

Systemd auto-mount units are config files located to the /etc/systemd/ and they're used for automount whenever the mount point is accessed.

The format of the config files is like this:
```bash
[Unit]
Description=Automount for the external data disk

[Automount]
Where=/mnt/external

[Install]
WantedBy=multi-user.target
```

After created the file systmd need to be restarted and star the unit:
```bash
systemctl daemon-reload
systemctl start mnt-external.automount
```

Now whanever the mount point is accessed the disk will be mounted.

Enabling automount at boot:
```bash
systemctl enable mnt-external.automount
```
___
## References
