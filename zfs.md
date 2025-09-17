

zfs-load-keyfile.service 
```
[Unit]
Description=Load ZFS Encryption Key
DefaultDependencies=no
Before=zfs-mount.service

[Service]
Type=oneshot
ExecStartPre=/bin/sleep 5
ExecStart=/usr/sbin/zfs load-key fourtb
RemainAfterExit=yes

[Install]
WantedBy=zfs-mount.service
```
