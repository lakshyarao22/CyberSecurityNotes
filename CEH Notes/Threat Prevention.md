# Threat Prevention

## Common Adversarial Behaviours

### Internal Recon

* Host discovery attempt
* Looking For Configuration
* Pivoting and lateral Movement
* Strange batch files
* Strange Power shell/bash commands

### Power shell use

Command line for windows which an attacker could use to gain access.

**[Living of the land](https://youtu.be/QBvM-MzQ570)** is a process in which we make use of whats available to us on machine and not install anything.

* Explore systems
* Connect to External Resources.
* Data Ex-filtration

### CLI/Terminal use

Look for Administrative commands run by normal users

### HTTP Request Headers

Manipulate the Headers to commands.

**Covert Channels** is ability to put commands that normal people are unable to see unless if they are Looking for it. Can be used for C2.

### WebShell use

If uploaded a script or program than attacker is able to access shell through Web Browser

### C2 use

Use of IoT Devices to attack

### DNS Tunneling

* DNS tunneling involves abuse of the underlying DNS protocol. Instead of using DNS requests and replies to perform legitimate IP address lookups, malware uses it to implement a command and control channel with its handler. DNS's flexibility makes it a good choice for data exfiltration; however, it has its limits.

### Data Staging

* Looking for sensitive data and packaging the it exfiltrate or destroy.

## Defence against the Adversarial Behaviours

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

### Categories of IOCs

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

* Anomalies in privilege user accounts
* Red-Flags on login activity
* Deviant DNS requests
* Increased Database Read volumes
* Sign of DDoS
* More requests than usual for same types of files
* unusual changes on Registry
* Abrupt patching

## Risks

Something which have a probability of negative outcome to asset

$$ Threats*Vulnerabilities*Impacts = Risk $$

$$ Threat*Vulnerabilities*Asset Value = Risk $$

$$ Impact * probability = Risk Level $$

* Low
  * There is a threat but its unlikely to occur
  * There is a threat but its Impact is negligible
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

|||||Severity|||
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|||Very Low|Low|Medium|High|Very High|
||Very High|💚|🔶|🔴|🔴|🔴|
||High|💚|🔶|🔶|🔴|🔴|
|Probability |Medium|💚|💚|🔶|🔶|🔴|
||Low|💚|💚|🔶|🔶|🔴|
||Very Low|💚|💚|💚|🔶|🔶|

## Risk Management

Creating a process to reduce risk to acceptable level.

### Objectives/Phases

* **Identification** or **Identify**: Identification of risk and its Impact
* **Prioritization** or **Asses**: Prioritize risks based on severity levels
* **Mitigation** or **Treat**: Control mitigate and prevent risk
* **Track and Review Risk**

## Cyber Threat Intelligence or CTI

Gathering, Processing and analysing the threat data to understand threats.

* Motives
* Targets and Goals
* Attack Behaviours

### Types of CTI

* **Strategic**: business strategies integrated with CTI ( Very high level ).
* **Operational**: CTIs related with specific attacks affecting the organisation. ( high level )
* **Tactical**: a more specific approach to CTIs i.e. If its a malware what type of malware it is. is it a RAT, is it a Trojan, etc. ( low level )
* **Technical**: more specific than Tactical. i.e. Hashes, Domains, etc. ( very low level )

## Threat Modeling

A systematized approach to threat and security.

* Know the enemy
* Know Us

### Process of threat Modeling

1. **Identifying Security Objectives**: What needs to be secure? OR Are there any policies?

2. **Application Overview**

    * Roles: Who will be using
    * Scenarios: Why using and what are normal usage.
    * How threat actor can misuse that?
    * What technologies are used in Application?
      * OS
      * Supporting apps and services
      * Network technologies
      * Ports and Services
    * Are there any security mechanisms involved
      * Authentication
      * Authorization
      * Access Control
      * Input Validation
      * Encryption

3. **Decomposing the Application**

    * Make a diagram of Flows
      * What are ins and outs for data
      * what are our trust boundaries.
      * How does data flows through system.

4. **Identifying Threats**

    * Identify Threat Actors
    * Identify APTs

5. **Identifying Vulnerabilities**

    * Know ourselves
    * Is there any convergence between Threats and Vulnerabilities.

### [Common Threat Modeling Methodology](https://www.eccouncil.org/threat-modeling/)

* STRIDE
* PASTA
* TRIKE
* VAST
* DREAD
* OCTAVE

## AI and ML in Cyber Security

AI is a ability's of a machine, computer or program to mimic Human Intelligence.

* Problem Solving
* Decision Making

Machine Learning is the ability to learn.

* **Supervised Data**: Labeled Dataset used for Learning or allowing a machine to learn.
* **Unsupervised Data**: Unlabeled data on which machine actually run its Intelligence and determine what is what

### Ml and AI are Solving ability to

* Classify and Categorize the data
* Automate intelligent monotonous Tasks
* Prediction
* Labeling unlabeled data based on its Analysis
* Finding Patterns in unlabeled Dataset
* Grouping data in manageable size

### Cyber Security Applications

* Abnormality detection
* Authentication
* Detect Phishing
* Threat detection
* Vulnerabilities Assessment
* Behavioural Analysis
* Network Security
* AI vs AI

## Standards and Regulations

* [PCI-DSS](https://www.pcisecuritystandards.org/document_library/)
* [ISO-IEC-27001](https://www.iso.org/isoiec-27001-information-security.html)
* [HIPPA](https://www.hhs.gov/hipaa/for-professionals/index.html)
* [Sarbanes Oxley Act](https://sarbanes-oxley-act.com/)
* [DMCA - Digital Millennium Copyright Act](https://www.dmca.com/FAQ/What-is-DMCA)
* [FISMA - FEDERAL INFORMATION SECURITY MODERNIZATION ACT](https://www.cisa.gov/federal-information-security-modernization-act)
* [GDPR](https://www.gdpreu.org/)
* [DPA](https://www.legislation.gov.uk/ukpga/2018/12/contents/enacted)
