## Clone a disk remotely:

Via telnet:
```bash
# DESTINATION:
nc -l -p 19000 | bzip2 -d | dd bs=16M of=file.img

# SOURCE:
dd bs=16M if=/dev/sda | bzip2 -c | nc 192.168.2.4 19000
```
Via SSH
```bash
# SOURCE:
dd bs=16M if=/dev/sda | ssh root@destination "dd bs=16M of=file.img"
```
###

##
