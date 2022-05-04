Add a device [it is good practice to perform a balance after this]
```btrfs device add -f /dev/sd[x] $MOUNTPOINT```

Remove a device
```btrfs device delete /dev/sd[x] $MOUNTPOINT```

Put device in degraded mode (e.g. broken)
```mount -o degraded /dev/sd[x] $MOUNTPOINT```

and then deletes via missing mode
```btrfs device delete missing $MOUNTPOINT```
