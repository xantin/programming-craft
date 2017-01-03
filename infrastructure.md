# Tips about infrastructure

I needed find if collectd is sending data to the network (specificly to another server)
I setup everthing as in tutorial and now what?
I found unix command [tcpdump](http://www.tcpdump.org/tcpdump_man.html) and I could test it collectd server sends data to another server.
I just run `sudo tcpdump -i any udp port 25826`




