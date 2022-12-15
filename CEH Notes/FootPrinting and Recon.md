# FootPrinting and Recon

**Active** :- Direct Interaction

**Passive** :- Without Direct Interaction

## What can be stealed?

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

### Tools

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
