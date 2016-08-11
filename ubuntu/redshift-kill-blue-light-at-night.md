# Kill blue light at night

This simple program kills blue light automatically 
using your timezone, which helps with working late 
at night. To install on Ubuntu:

```
sudo apt-get install redshift redshift-gtk
alias redshift='gtk-redshift -l 37.421:-122.090 &' 
redshift
```

You will have to update the coordinates to reflect
your real location.

Thanks to @rezama for pointing this out.
