# UCF-WPA2-Enterprise-Raspberry-Pi
This is the required fix and code for the wpa_supplicant.conf file to connect to the University of Central Florida's enterprise wireless system on a Raspberry Pi (and most Debian systems).

# Fix Driver for Raspberry Pi Buster

Go to this file:
```
/lib/dhcpcd/dhcpcd-hooks/10-wpa_supplicant
```

Look for a line with:
```
wpa_supplicant_driver="${wpa_supplicant_driver:-nl80211,wext}"
```

Swap the order of the drivers to this:
```
wpa_supplicant_driver="${wpa_supplicant_driver:-wext,nl80211}"
```

# wpa_supplicant.conf

Check wpa_supplicant.conf file uploaded. Replace "NID" with your personal NID. Replace "NIDpassword" with your personal NID password.
