# Git: Ignoring CHMOD mode changes

Sometimes Git will detect CHMOD changes on Ubuntu while syncing between 2 different machines. To avoid the problem, disable the core.fileMode option in git config: 

```
git config --global core.fileMode false
```
