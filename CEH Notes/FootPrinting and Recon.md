# FootPrinting and Recon

**Active** :- Direct Interaction

**Passive** :- Without Direct Interaction

## What can be stolen?

* System Information
* Username and passwords
* DNS and firewall
* Organizational Information
* Vulnerability identification

## Google Dorks

"Search Full String"

use **-Info** to remove "info" from search output

## Tools for Google Hacking

[Google dorks List](https://securitytrails.com/blog/google-hacking-techniques)

[Google Hacking Database](https://www.exploit-db.com/google-hacking-database)

[Google Dorks Database](https://www.boxpiper.com/posts/google-dork-list)

## [Shodan](https://www.shodan.io/) And [Censys](https://search.censys.io/)

Shodan is used to find open ports vulnerabilities etc. on an IP or domain.

Similarly, we can use Censys to find hosts, IP Address, etc.

## Sub-Domain Enumeration

It is the practice of checking subdomains from list of common domains One-By-One.

``` text
        ____ Registered Domain
       v
docs.google.com
  ^          ^
  |          |______Top-Level Domain
  |__Sub Domain
```

### Tools for Subdomain Enumeration

* [Netcraft](https://www.netcraft.com/tools/)
* [Sublist3r](https://github.com/aboul3la/Sublist3r) for subdomain enumeration
* [ARIN](https://www.arin.net/) used to get info for
* [RDAP](https://www.icann.org/rdap)
* [TraceRoute](https://www.fortinet.com/resources/cyberglossary/traceroutes) to see path of traffic.
* [Path Analyzer Pro](https://download.cnet.com/Path-Analyzer-Pro-Windows/3000-2085_4-10620979.html) used to see path of traffic.
* [Foca](https://github.com/ElevenPaths/FOCA) to find metadata in Files (Metadata recon)
* [OSINT](https://osintframework.com/)
* [Recon-Dog](https://github.com/s0md3v/ReconDog) is used to extract info through APIs, No direct connection to Target.
* [Maltego](https://www.maltego.com/) used for Mind Map
* [Recon-NG](https://www.kali.org/tools/recon-ng/) Metasploit for OSINT.
* [TheHarvester](https://www.kali.org/tools/theharvester/) The tool gathers names, emails, IPs, subdomains, and URLs by using
multiple public resources

## Tools for location Recon

* [Google Maps](https://www.google.com/maps)
* [Wikimap](https://wikimapia.org/##lang=en&lat=0.000000&lon=0.000000&z=12&m=w)

## Job Posting Recon

Job postings can be used to determine the technologies of a organization.

* [Monster.com](https://www.monster.com/)
* [LinkedIn](https://www.linkedin.com/jobs/)

## Metadata Recon

Metadate is **Data** about **Data**

### Tools to gather metadata

#### [Metagoofil](https://www.kali.org/tools/metagoofil/)

It is a tool to automate the process of gathering files from a website.

```bash
metagoofil -d itpro.tv -e 200 -t pdf,doc,txt
   ^            ^          ^      ^
Program      Website     Delay  Filetypes
```

#### [Exiftool](https://exiftool.org/)

A tool which extract all the metadata from a file.

#### [Exifdata](https://exifdata.com/)

An Online Exiftool Alternative.

#### [Strings](https://en.wikipedia.org/wiki/Strings_(Unix))

Similar tool like Exiftool built into Linux.

## WordLists

A List of words, One word per line.

### Most Common Wordlists

* [SecList](https://github.com/danielmiessler/SecLists)
* [rockyou](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjQxpu5xbj8AhWXyzgGHaD3DoEQFnoECBMQAQ&url=https%3A%2F%2Fgithub.com%2Fbrannondorsey%2Fnaive-hashcat%2Freleases%2Fdownload%2Fdata%2Frockyou.txt&usg=AOvVaw3snAERl1mU6Ccr4WFEazBd)

### Custom Wordlists

* [Cewl](https://www.kali.org/tools/cewl/)
This program makes custom wordlist based on a website you give to it.

```bash
cewl -m 6 -o -w wordlist.txt itprotv
        ^          ^           ^
     min words   outputTo    Website
```

## Email Tracking

Info gathered with email tracking.

* Proxy use
* IP Address
* Geo Location
* How long it took to read email
* Where links clicked
* OS Type
* Browser Type
* Host device type

Uses a 1x1 image block embedded inside mail coded with a program

### Tools used for email tracking

* [Infoga](https://github.com/m4ll0k/Infoga)
* [Bitly](https://bitly.com/)
* [Linkly](https://linklyhq.com/)

## [WhoIs](https://www.whois.com/) and DNS Recon

* Thick WhoIs: All Info
* Thin WhoIs: Faster

### DNS Tools

* [nslookup](https://www.kali.org/tools/bind9/#nslookuphttps://linux.die.net/man/1/nslookup)
* [dig](https://www.kali.org/tools/bind9/#dig)
* [dnsrecon](https://www.kali.org/tools/bind9/#dnsrecon)

## Protection Against Recon

* Find wrong and make policy and procedure
* Training and Awareness
* [Who.is](https://who.is/) privacy services
* [Encryption](https://www.techtarget.com/searchsecurity/definition/encryption#:~:text=Encryption%20is%20the%20method%20by,encrypted%20data%20is%20called%20ciphertext.)
* Be paranoid on social Media
* Disable location services
* Sanitize job listings

### Tools To Protect Against Recon

* [Freenet](https://freenetproject.org/index.html)
* [RetroShare](https://retroshare.cc/)
* [Tor Browser](https://www.torproject.org/download/)
* [Tails OS](https://tails.boum.org/)
* [Hidden WiKi](https://thehiddenwiki.org/)

