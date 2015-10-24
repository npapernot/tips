# Permission Error after Using `sudo` to run Git

To fix the permission error, move to `/repo-root/.git/` and change the permissions by:

```
sudo chmod -R g+ws *
``` 
