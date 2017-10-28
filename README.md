# unix-commands
Unix commands to remember

## Disks
- `fdisk -l` - list disks
- `umount /dev/sdX` - unmount a disk
- `sudo shred -v -n1 -z /dev/sdX` - securely(ish) erase the contents of /dev/sdX 
- `mkfs -t ext4 /dev/sdXn` - add a filesystem
- `mount /dev/sdx1 /storage` - mount device in directory

## Files and directories
- `tar -zcvf archive-name.tar.gz directory-to-be-compressed` - Compress directory, options: z:gzip, c:create archive, v:verbose output, f:name
- `tar -zxvf archive-name.tar.gz` - Uncompress and archive the output of the above

## Networking
- `sudo netstat -nlp | grep LISTEN` - Which services are listening on which ports?

### OSX/macOS specific
- `sudo lsof -i | grep LISTEN` - Which services are listening and on which ports?

## Tricks of the trade
- `while [ $? -eq 0 ]; do npm test -s; done` - Do something until failure occurs (typically run flakey tests)
- `yes 'You are a UNIX god' | xargs say` - Have fun, ideally at the expense of your friends
