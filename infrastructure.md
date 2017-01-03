# Tips about infrastructure

## network sniffer
I needed to find if collectd is sending data out to the network (specifically to another server)
I set up everthing as in tutorial and the question was "what now"?
I found unix command [tcpdump](http://www.tcpdump.org/tcpdump_man.html) and I could test if collectd server sends data to another server.
I just run `sudo tcpdump -i any udp port 25826`

## monitoring your servers

After long-time-consuming digging I discovered program name [collectd](https://collectd.org/).
You can really fast set it up and run it. It has multiple plugguins e.i. cpu and memory usage.
[Very good tutorial](https://blog.laputa.io/try-influxdb-and-grafana-by-docker-6b4d50c6a446#.9gx6os1fx)
[Here are useful scrips](https://github.com/vishal-biyani/collectd-influxdb-grafana/tree/master/scripts)

### set up (unix)

`sudo apt-get update` 

`sudo apt-get -y install collectd collectd-utils`

collectd configure file is located in `/etc/collectd/collectd.conf`




