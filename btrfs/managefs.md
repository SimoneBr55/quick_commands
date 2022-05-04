Resize fs
```btrfs filesystem resize $DEVICE_ID [+/-] $NEW_SIZE $FILESYSTEM```

Fill a device
```btrfs filesystem resize $DEVICE_ID max $FILESYSTEM```

Balance a fs
```btrfs balance start $MOUNTPOINT```
```btrfs balance status $MOUNTPOINT```

Defragment file or folder
```btrfs filesystem defragment $PATH```

Scrub (remove errors and rottenbits) [it has low IO priority]
```btrfs scrub start $MOUNTPOINT```
```btrfs scrub status $MOUNTPOINT```
