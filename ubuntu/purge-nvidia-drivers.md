# Remove all nvidia drivers

To purge all nvidia drivers from Ubuntu:

```
sudo apt-get remove --purge nvidia-*
```

Then, add `nouveau` at end of file `/etc/modules` and reboot.


Adapted from (http://askubuntu.com/questions/206283/how-can-i-uninstall-a-nvidia-driver-completely)
