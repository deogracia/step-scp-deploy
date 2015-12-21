# step-scp-deploy
wercker deploy step : publish your files via scp

# Options
* host => The server to connect to
* sshport (optional) => The ssh port to connect to.  Default value is ''22''
* sshprivatekey => The SSH identity to use
* user => The name of the user
* source (optional) => the directory to push to your server. Default value is ''${WERCKER_OUTPUT_DIR}''
* destination => the remote directorys
* hide-ssh-cnx-info-from-log => don't display SSH cnx info (USER, port etc.) from log.  Default value is ''true'' (I don't want these info to be easily readable)

# Example
```
- scp-deploy:
    host: example.org
    sshport: 12345
    sshprivatekey: $PRIVATEKEY_FILE
    user: myuser
    source: "${WERCKER_OUTPUT_DIR}/public"
    destination: "/var/www"
    hide-ssh-cnx-info-from-log: false
```
