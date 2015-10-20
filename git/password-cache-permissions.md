# Password Cache Permissions

When the github command `git` cannot access the password cache and gives the
following error: `fatal: unable to connect to cache daemon: Permission denied`,
use the following chown to fix the permissions on github cache: 

`sudo chown [username] ~/.git-credential-cache/`

where [username] is the OS username from the machine cloning.
