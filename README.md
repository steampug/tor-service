# tor-service
Customized Tor config &amp; systemd service file

I didn't like the service file and config that Tor ships with in the official Archlinux package anyway, so I've been using my own variation. Rather than relying on tor to decide which user it's running as, that's handled by systemd. Furthermore systemd creates a directory restricted to the tor user and makes a read-only copy of the torrc from /etc/torrc every time the service is started.

I'm sure there are many ways this concept could be improved on (firejail, lxc, etc...) but I just thought the stock tor service file left something to be desired for all the features systemd offers now.

Enjoy
