# Compiz slowing GUI after Nvidia driver update

When Nvidia driver update causes GUI to lag, and 
`top` identifies `compiz` as using high CPU ressources,
an easy fix (if compiz is not needed) is to use
the previous gnome version. Install it using

```
sudo apt-get install gnome-session-flashback
```

and then lgout, click on the ubuntu icon close
to the password field, select the option with 
`metacity` and login. 
