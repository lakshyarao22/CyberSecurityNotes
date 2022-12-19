# Scanning

## Host Discovery

Used to find the usable targets and their OS.

### Tools

* **Ping** send ICMP request
* Angry IP scanner (GUI)
* [Nmap](https://nmap.org/) ([Manual](https://linux.die.net/man/1/nmap))
  **nmap -sL 45.33.32.0/28** (List scan)

### Countermeasures

* IDS
* IPS
* snort
* ACL
* DMZ
* firewall

## Port and service scanning

Used to get open ports and running services. Also versioning Information of running services.

### Critical Ports

* 21 ftp
* 22 ssh
* 23 telnet
* 25 SMTP
* 53 DNS
* 80 HTTP
* 111 rpcbind
* 139 netbios-ssn
* 445 microsoft-ds
* 512 exec
* 513 login
* 514 shell
* 1099 rmiregistry
* 1524 ingreslock
* 2049 nfs

## Vulnerability Scanning

As name explains used to get Vulnerabilities on running services.

## TCP Communications

### Control Flags

* **SYN** Synchronize :-
  Used to initialize the connection
* **ACK** Acknowledgment :-
  Host is Ready
* **FIN** Finish :-
  Transmission is over
* **RST** Reset :-
  Error has occurred
* **PSH** Push :-
  Used to buffer data to speed up transmission
* **URG** Urgent :-
  This is priority data

### Three-way handshake

```Text
_______                       _______
|     |  SYN -->              |     |
|_____|         <-- SYN-ACK   |_____|
   A     ACK -->                 B
```

We can use [WireShark](https://www.wireshark.org/) to See communications

## Network Scanning Tools

* [Nmap](https://nmap.org/) ([Manual](https://linux.die.net/man/1/nmap)) good for local network (slow)
* [Unicornscan](https://www.kali.org/tools/unicornscan/) ([Manual](https://linux.die.net/man/1/unicornscan)) faster than Nmap
* [masscan](https://github.com/robertdavidgraham/masscan) faster for over the internet
* [hping3](https://www.kali.org/tools/hping3/) ([Manual](https://linux.die.net/man/1/hping3))

### Mobile scanners

* [Fing](https://play.google.com/store/apps/details?id=com.overlook.android.fing&hl=en_IN&gl=US)
