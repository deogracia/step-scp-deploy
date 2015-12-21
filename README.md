# step-scp-deploy
wercker deploy step : publish your files via scp

# Options
* host => The server to connect to
* sshport (optional) => The ssh port to connect to.  Default value is ''22''
* sshprivatekey => The SSH identity to use
* user => The name of the user
* source (optional) => the directory to push to your server. Default value is ''${WERCKER_OUTPUT_DIR}''
* destination => the remote directorys

# Example
```
- scp-deploy:
    host: example.org
    sshport: 12345
    sshprivatekey: $PRIVATEKEY_FILE
    user: myuser
    source: "${WERCKER_OUTPUT_DIR}/public"
    destination: "/var/www"
```
