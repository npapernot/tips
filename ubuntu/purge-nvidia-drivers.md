# Remove all nvidia drivers

To purge all nvidia drivers from Ubuntu:

```
sudo apt-get remove --purge nvidia-*
```

Then, add `nouveau` at end of file `/etc/modules` and reboot.
