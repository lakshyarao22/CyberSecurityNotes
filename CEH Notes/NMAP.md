# NMAP Scans

## IDLE/IPID Scan

It is an indirect scan in which an intermediate host(ZOMBIE) is used to scan a target.

* **ZOMBIE**:- An Intermediate Host on same network as target.

Q: How to Verify a good zombie?
A: A good zombie is a host which don't have too much traffic going from or to itself. Like an Network Printer as its online always and dont have too much traffic going through it. Like one or two prints in a day.

## Verification of good Zombie

We Verify a good zombie by sending a SYN-ACK packet to it. **(NOT SYN)**

```text
_______                       _______
|     |  SYN-ACK -->          |/   \|
|_____|         <-- RST       |_____|
   A                             B
```

* As There is no active connection to Printer the printer will send a RST Packet with an IPID lets take it to be 1182

* Again send a SYN-ACK to printer to verify. If the IPID is incremental i.e. 1183 that means we have a good zombie as it don't have too much traffic running through it.

* We can use IPID as a reference and send SYN-ACK packet to target machine.

* Now again check if IPID is update. If not then it means that host is not active or port not open.
