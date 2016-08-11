# Kill blue light at night

This simple program kills blue light automatically 
using your timezone, which helps with working late 
at night. To install on Ubuntu:

```
sudo apt-get install redshift redshift-gtk
redshift
```

You will have to update the coordinates to reflect
your real location.

Thanks to @rezama for pointing this out.

If you are having problems with automatically
detecting your timezone, you can use the following
to enter them automatically

```
alias redshift='gtk-redshift -XXX.XXX:-YYYYYY &' 
```
