#  Unix [unix-useful-commands](https://www.tutorialspoint.com/unix/unix-useful-commands.htm)

Here will be summary of me known commands

## delete install program from unix

`sudo apt-get purge PROGRAM_NAME
sudo apt-get autoremove --purge PROGRAM_NAME
sudo apt-get autoclean`

## openssl [doc](https://linux.die.net/man/1/openssl)

OpenSSL is a cryptography toolkit implementing the Secure Sockets Layer ( SSL v2/v3) and Transport Layer Security ( TLS v1) network protocols and related cryptography standards required by them.

Use cases 

*  Creation and management of private keys, public keys and parameters
*  Public key cryptographic operations
*  Creation of X.509 certificates, CSRs and CRLs
* Calculation of Message Digests
*  Encryption and Decryption with Ciphers
*  SSL/TLS Client and Server Tests
*  Handling of S/MIME signed or encrypted mail
*  Time Stamp requests, generation and verification

## type [doc](http://linuxcommand.org/lc3_man_pages/typeh.html)
type is a command that describes how its arguments would be interpreted if used as command names.
 
`type command_name`

e.i. `type nodejs`

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

for copy directory use `scp -r user@server1:/path/to/folder user@server2:/where/to/put`

## jobs [more about working with processes](https://kb.iu.edu/d/afnw)
Lists the status of all running background jobs.

`jobs`

with command *fg number_of_process* you move process form background to foreground and than you can kill it with ctrl + c

## port forwarding [doc](https://linux.die.net/man/1/ssh)

`ssh -nNT -L host_post:remove_host_name:remove_port username@server_name`

e.i. `ssh -nNT -L 9000:localhost:5432 user@example.com`

## man [online version of man](https://linux.die.net/man/)
The man Command. The man command is used to format and display the man pages. The man pages are a user manual that is by default built into most Linux distributions (i.e., versions) and most other Unix-like operating systems during installation.

e.i. `man ssh`
