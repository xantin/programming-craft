#  Unix

Here will be summary of me known commands

## lsb_release [doc](https://linux.die.net/man/1/lsb_release)
print distribution-specific information

`lsb_release`

e.i. `lsb_release -a`

## uname [doc](https://linux.die.net/man/1/uname)
print system information

`uname`

e.i. `uname -s`

## scp [doc](https://linux.die.net/man/1/scp)
copies files between hosts on a network

`scp user@server1:/path/to/file user@server2:/where/to/put`

## jobs [more about working with processes](https://kb.iu.edu/d/afnw)
Lists the status of all running background jobs.

`jobs`

## port forwarding [doc](https://linux.die.net/man/1/ssh)

`ssh -nNT -L host_post:remove_host_name:remove_port username@server_name`

e.i. `ssh -nNT -L 9000:localhost:5432 user@example.com`

## man [online version of man](https://linux.die.net/man/)
The man Command. The man command is used to format and display the man pages. The man pages are a user manual that is by default built into most Linux distributions (i.e., versions) and most other Unix-like operating systems during installation.

e.i. `man ssh`
