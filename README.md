# unix-commands
Unix commands to remember

## Files and directories
`tar -zcvf archive-name.tar.gz directory-to-be-compressed` - Compress directory, options: z:gzip, c:create archive, v:verbose output, f:name

## Networking
`sudo netstat -nlp | grep LISTEN` - Which services are listening on which ports?

### OSX/macOS specific
`sudo lsof -i | grep LISTEN` - Which services are listening and on which ports?
