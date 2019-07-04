# wpa2-hacking
Little project to obain WPA2 keys with social engineering.

You will need aircrack-ng to disconnect the victim from his access point with aireplay.

Creates a fake access point in WPA2, similar to the victim's access point.
Once the victim is disconncted from his access point, he will try to connect to the rogue AP. The victim will be connected to the WPA2 rogue AP with the WPS push button.

After that, the victim can browse the internet but every http page will be redirected to our web server asking for WPA2 password for an "update".
The WPA2 password will be logged in /var/log/apache2/access.log.

At this point we stop the attack and can connect to the real access point of the victim.
