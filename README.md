# FreeBSD template

## How to
1. Install minimum FreeBSD installation
2. By default, sendmail is installed, it's not needed, deactive by adding the following line to /etc/rc.local:
    sendmail_enable="NONE"
3. By default, again, FreeBSD has multiple virtual consoles enabled (https://www.freebsd.org/doc/handbook/consoles.html). Each takes about 10M memory and usually is just idle. Disable them by uncommenting all except for the first one in /etc/ttys
4. Change shell login message by editing file /etc/motd.template
   (https://man.freebsd.org/cgi/man.cgi?motd)

By now, you should have a very slim and performant system with just ~500MB disk
footprint and minimum memory usage of ~75MB.


## Using ports
Install ports by $ pkg update

## Installing Python
5. Install python by $ pkg install lang/python3.9
6. Create an alias for python -> python 3.9

## Updates
FreeBSD divides the software installed into the base system and applications.
The first one is handled by using $ freebsd-update, and the other one via ports.
All external applications, should to greatest extent possible, be installed via
ports for easiest maintenance. 

### Base system
Run
$ freebsd-update fetch
$ freebsd-update install

Reboot system if needed afterwards

### Applications
Run
$ pkg update
$ pkg upgrade

## Logs
Logs are located in /var/log directory.
Sytem logs more specifically /var/log/messages.
