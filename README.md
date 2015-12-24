# socks-cmd

socks modify binaries from the [pac-cmd](https://github.com/getlantern/pac-cmd) project.

A command line tool to change proxy socks settings of operation os x system.

Note - you will need to run make separately on each platform.

# Install

```sh
gcc -Wall -c -D DARWIN -D AMD64 -x objective-c main.c common.h
gcc -o socks main.o -framework Cocoa -framework SystemConfiguration -framework Security
```

# Usage

```sh
socks <on | off> <ip> <port>
```

#Notes

*  **Mac**
  
Setting socks is an privileged action on Mac OS. `sudo` or elevate it as below.

There's an additional option to chown itself to root:wheel and add setuid bit.

```sh
socks setuid
```