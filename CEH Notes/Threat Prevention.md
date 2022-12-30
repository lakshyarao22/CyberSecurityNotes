# Threat Prevention

## Common Adversarial Behaviours

### Internal Recon

* Host discovery attempt
* Looking For Configuration
* Pivoting and lateral Movement
* Strange batch files
* Strange Powershell/bash commands

### Powershell use

Command line for windows which an attacker could use to gain access.

**[Living of the land](https://youtu.be/QBvM-MzQ570)** is a process in which we make use of whats available to us and not install anything.

* Explore systems
* Connect to External Resources.
* Data Exfiltration

### CLI/Terminal use

Look for Administrative commands run by normal users

### HTTP Request Headers

Manupulate the Headers to commands.

**Covert Channels** is ability to put commands that normal people are unable to see unless if they are Looking for it. Can be used for C2.

### WebShell use

If uploaded a script or program than attacker is able to access shell through Web Browser

### C2 use

Use of IoT Devices to attack

### DNS Tunneling

* DNS tunneling involves abuse of the underlying DNS protocol. Instead of using DNS requests and replies to perform legitimate IP address lookups, malware uses it to implement a command and control channel with its handler. DNS's flexibility makes it a good choice for data exfiltration; however, it has its limits.

### Data Staging

* Looking for sensetive data and packaging the it exfiltrate or destroy.

## Defence against tbe Adversarial Behaviours

* WAF
* Whitelist and Blacklist
* Risk Analysis
* Manual Inspection of Logs
* Block known keys and domains that are Malicious with use of firewall.
* Monitor DNS and look for spikes in DNS traffic
* File logging and DLP


## Threat Hunting concepts

### Define

Assume data is system is already under attack or data breach then look for related indicators.

### Come up with a Hypothesis

Make a Hypothesis that what types of attackers we have based on working of organisation. Finding vulnerabilities and TTP of potential attacker.

Creating an IR before actual attack.

## IoC

Indicators of Compromise are indicators which point towards a security breach.

### Types of IOCs

* **Atomic** :- Self contained data
    * IP address
    * Email address

* **Computed** :-
    * Hash values
    * Regex

* **Behavioural**
    * Logical combining of the Atomic and Computed IOCs

### Catagories of IOCs

* **Email** : Comprised of email artifacts
    * Sender's email address
    * Subject line 
    * Attachments
    * Links

* **Network**
    * Domain Info
    * IP address

* Host Based
    * File Names
    * Hash values
    * Registry Entries
    * dll or drivers

* Behavioural
    * Macros running Powershell
    * Service accounts behaving as a user would

### Examples

* Anomalies in privilage user accounts
* Red-Flags on login activity
* Diviant DNS requests
* Increased Datebase Read volumes
* Sign of DDoS
* More requests than usual for same types of files
* unusual changes on Registry
* Abrupt patching

## Risks

Something which have a probability of negative outcome to asset

```math

Threats * Vulnerabilities * Impacts = Risk
```

```math

Threat * Vulnerabilities * Asset Value = Risk
```

```math

Impact * probability = Risk Level

```

* Low
    * There is a threat but its unlikely to occure
    * There is a threat but its Impact is neglegible
* Medium
    * Threat is likely but not imminent
    * You have some time but its about to hit
    * Mitigate asap to reduce risk/Impact
* High
    * Take IMMEDIATE action
    * Threat is about to hit

### Risk Matrix

* High is Red 🔴
* Mid is Orange 🔶
* Low is Green 💚

| | |  | | Severity | | |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| | | Very Low | Low | Medium | High | Very High |
| | Very High | 💚  | 🔶 | 🔴 | 🔴 | 🔴 |
| | High | 💚 | 🔶 | 🔶 | 🔴 | 🔴 |
|Probability | Medium | 💚 | 💚 | 🔶 | 🔶 | 🔴 |
| | Low | 💚 | 💚 | 🔶 | 🔶 | 🔴 |
| | Very Low | 💚 | 💚 | 💚 | 🔶 | 🔶 |

