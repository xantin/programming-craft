#  Unix

Here will be summary of me known commands

## scp [doc](https://linux.die.net/man/1/scp)
copies files between hosts on a network

`scp user@server1:/path/to/file user@server2:/where/to/put`

## jobs [more about working with processes](https://kb.iu.edu/d/afnw)
Lists the status of all running background jobs.

`jobs`

## port forwarding [doc](https://linux.die.net/man/1/ssh)

`ssh -nNT -L host_post:remove_host_name:remove_port username@server_name`

example `ssh -nNT -L 9000:localhost:5432 user@example.com`


