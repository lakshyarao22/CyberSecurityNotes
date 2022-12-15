# Hacking Basics

## Threats

### Threat Maps

* [FireEye](https://www.fireeye.com/cyber-map/threat-map.html)
* [CheckPoint](https://threatmap.checkpoint.com/)
* [Other Threat Maps](https://www.google.com/search?q=threat+map)
  
**0day** :- Threats Unknown to Manufacturer Or Still do not have Patches.

**doxing** :- releasing private info to public.

**Bot** :- Machines which is remotely controlled.

**Bot Net** :- Mesh of Bots.

## CIA Triad

**Confidentiality** :- Data not seen by unauthorized.

**Integrity** :- Data should not change.

**Accessibility** :- One who could Access should be able to access the data any time.

## Hacker's job is to:-

Breach - Confidentiality

Disintegrate - Integrity

Reduce Accessibility

**Authenticity** :- used to verify integrity.

## Security Triangle

``` Text
                 Security
                     A
                    / \
                   /   \
                  /  O  \
                 /       \
                /_________\
  Functionality             Usability
```

These 3 things should be balanced

**Attack Vector** :- The doorway to attack a system.

**Threat Actor** :- Creator of Threat.

## **Threat** is something which has possibility of **exploit** against a **vulnerability**

### Threat Catagories

### Network Threats

* MITM(Man In The Middle)
* DoS / DDoS
* DNS / ARP Poisoning
  
## Host Threats

* Password Cracking
* Malware
* Privilege Escalation
* Code Execution
  
## Application Threats 

* Injection attacks
* Buffer Overflow
* Security Misconfigurations
  

**APT** :- Advanced Persistent Threats

## Types Of Security

### Defensive

### Offensive

* Annoyance e.g. Honeypots
* attribution e.g. Web Bug
* Attack

## Types of Hackers

* **Black Hat** :- use Knowledge for malicious intent
* **Grey Hat** :- use Knowledge for both malicious intent and good intent
* **White Hat** :- use Knowledge for good intent
* **Suicide Hackers** :- Who want to watch the system go down
* **Script Kiddies** :- Who do not have in-depth knowledge about computers and Hacking.
* **Cyber Terrorist** :- Who cause loss of Life
* **State Sponsored** :- Who protect country and its allies and attack enemy.
* **Hacktivists** :- It is the act of hacking, or breaking into a computer system, for politically or socially motivated purposes.
  
## Hacking Phases

1. [Recon](FootPrinting%20and%20Recon.md)
   * Passive
     * [Social Engineering](Social%20Engineering.md)
   * Active
     * [Social Engineering](Social%20Engineering.md)
2. Scanning
   * Find Ports and Services
   * Find Hosts
   * Find OS
   * Find Vulnerabilities
3. Gaining Access
   * Privilege escalation
   * Cracking passwords
4. Maintaining Access
   * Installing Malware and rootkits
5. Covering Up tracks
   * Modifying logs
   * Hiding malware

## Cyber kill chain

1. **Reconnaissance**:- Research, identification, and selection of targets.
2. **Weaponization**:- Pairing remote access malware with exploit into a deliverable payload (e.g., Adobe PDF and Microsoft Office files).
3. **Delivery**:- Transmission of weapon to target (e.g., via email attachments, websites, or USB drives).
4. **Exploitation**:- Once delivered, the weapon’s code is triggered, exploiting vulnerable applications or systems.
5. **Installation**:- The weapon installs a backdoor on a target’s system, allowing persistent access.
6. **Command and Control**:- Outside server communicates with the weapons providing “hands-on keyboard access” inside the target’s network.
7. **Action and Objective**:- The attacker works to achieve the objective of the intrusion, which can include exfiltration or destruction of data, or intrusion of another target.