# unix-commands
Unix commands to remember

## Disks
- `fdisk -l` - list disks
- `umount /dev/sdX` - unmount a disk
- `sudo shred -v -n1 -z /dev/sdX` - securely erase the contents of /dev/sdX for flash media, -n 7 for magnetic
- `mkfs -t ext4 /dev/sdXn` - add a filesystem
- `mount /dev/sdx1 /storage` - mount device in directory

## Files and directories
- `tar -zcvf archive-name.tar.gz directory-to-be-compressed` - Compress directory, options: z:gzip, c:create archive, v:verbose output, f:name
- `tar -zxvf archive-name.tar.gz` - Uncompress and archive the output of the above

## Networking
- `sudo netstat -nlp | grep LISTEN` - Which services are listening on which ports?

### SSH Tunnel
Bind port 8000 on the machine on which you run the command to port 8000 on machine at 1.2.3.4
- `ssh -i ~/.ssh/key.pem -L 8000:localhost:8000 user@1.2.3.4` (bind to localhost only)
- `ssh -i ~/.ssh/key.pem -L \*:8000:localhost:8000 user@1.2.3.4` (publically available)

### OSX/macOS specific
- `sudo lsof -in | grep LISTEN` - Which services are listening and on which ports?

## Tricks of the trade
- `while [ $? -eq 0 ]; do npm test -s; done` - Do something until failure occurs (typically run flakey tests)
- `yes 'You are a UNIX god' | xargs say` - Have fun, ideally at the expense of your friends

## Git
`git config --global alias.logr "log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset%n' --abbrev-commit --date=relative --branches --decorate --all"`
