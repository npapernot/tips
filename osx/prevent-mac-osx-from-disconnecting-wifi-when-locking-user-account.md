# Prevent a Mac from disconnecting WiFi upon account lock

If your Mac disconnects the WiFi adapter after you lock your computer and it
goes to the lock screen, you can disable that behavior by setting a preference
in the Airport utility. Perform the following in the terminal:

```
cd /System/Library/PrivateFrameworks/Apple80211.framework/Versions/Current/Resources
sudo ./airport <wifi interface> prefs DisconnectOnLogout=NO
```

Replace `wifi interface` by the name of the network interface that corresponds
to your Wifi Adapter. You can find that out by running an `ifconfig` command. 

