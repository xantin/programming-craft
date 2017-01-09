# Tips about infrastructure

* [network sniffer](#network-sniffer)
* [monitoring your servers](#monitoring-your-servers)
* [set up (unix)](#set-up-unix)
* [check out if tunnel is open](#check-out-if-tunne-is-opened)
* [how to find out if command is running?](#how-to-find-out-if-command-is-running)
* [transport data between 2 streams](#transport-data-between-2-streams)


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

used tools:

* collectd with plugins (network pluging for sending data out of local machine)
* influxdb for storing timeseries data, I like design this database, but should try to use another one as well
* grafana for nice presentation data (is very mature that is why I used it instead of chronograf)

One thing about Influxdb is very bad and it's no clustering at all, why is bad => not so easy horizontal scale.

### check out if tunnel is opened
`nc -z localhost 6000 || echo 'no tunnel open'`

### how to find out if command is running?
use htop tool `apt-get install htop` and search (F3) your command.
This way you can find runing open ssh tunnel and close it

### transport data between 2 streams
[socat](https://linux.die.net/man/1/socat)
`socat -T15 udp4-recvfrom:25826,reuseaddr,fork tcp:localhost:4444 &`

examplete transports UDP 25826 to TCP 4444
