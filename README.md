# TryHackMe-Cyber-Kill-Chain

## Task 1: Introduction

The term **Kill Chain** is a military concept related to the structure of an attack. It consists of:
1. Target identification
2. Decision and order to attack the target
3. Target destruction

**Lockheed Martin**, a global security and aerospace company, established the **Cyber Kill Chain®** framework for the cybersecurity industry in 2011 based on this military concept. The framework defines the steps used by adversaries or malicious actors in cyberspace. To succeed, an adversary needs to go through all phases of the Kill Chain.

## Task 2: Reconnaissance

**Reconnaissance** involves discovering and collecting information on the system and the victim. It is the planning phase for the adversaries.

### OSINT (Open-Source Intelligence)
OSINT is the first step an attacker needs to complete to carry out further phases of an attack. The attacker studies the victim by collecting available information on the company and its employees, such as:
- Company size
- Email addresses
- Phone numbers from public resources

**Email harvesting** is the process of obtaining email addresses from public, paid, or free services. It is used for phishing attacks.

#### Tools for Reconnaissance:
- **theHarvester**: Gathers emails, names, subdomains, IPs, and URLs using multiple public data sources.
- **Hunter.io**: An email hunting tool for obtaining contact information associated with the domain.
- **OSINT Framework**: Provides a collection of OSINT tools based on various categories.

**Question:** What is the name of the Intel Gathering Tool that is a web-based interface to the common tools and resources for open-source intelligence?
**Answer:** OSINT Framework

**Question:** What is the definition for the email gathering process during the stage of reconnaissance?
**Answer:** Email harvesting

## Task 3: Weaponization

After successful reconnaissance, the adversary crafts a "weapon of destruction" without directly interacting with the victim. This involves combining malware and exploit into a deliverable payload.

- **Malware**: A program designed to damage, disrupt, or gain unauthorized access to a computer.
- **Exploit**: A program/code that takes advantage of a vulnerability in the application or system.
- **Payload**: Malicious code that the attacker runs on the system.

**Term for group of commands performing a specific task, often used maliciously in Microsoft Office documents:**
**Answer:** Macro

## Task 4: Delivery

The Delivery phase involves transmitting the payload or malware. Methods include:

1. **Phishing email**: Targeting specific individuals (spearphishing) or multiple people in a company with a malicious email containing a payload.
2. **Infected USB drives**: Distributed in public places.
3. **Watering hole attack**: Compromising a website frequently visited by a target group, redirecting them to a malicious site.

**Question:** What is the name of the attack when it is performed against a specific group of people, aiming to infect a frequently visited website?
**Answer:** Watering hole attack

## Task 5: Exploitation

Exploitation involves leveraging vulnerabilities to gain system access. Techniques include:
- **Phishing links and macro attachments**: Leading to fake login pages or executing ransomware.
- **Lateral movement**: Techniques used to move deeper into a network after gaining initial access.
- **Zero-day Exploit**: Exploits unknown vulnerabilities, leaving no opportunity for initial detection.

**Question:** What is the term for a cyberattack targeting a software vulnerability unknown to antivirus or software vendors?
**Answer:** Zero-day

## Task 6: Installation

Upon gaining access, attackers install persistent backdoors to maintain access even if detected or removed initially.

- **Web shell**: Malicious script on a webserver to maintain access.
- **Meterpreter**: A Metasploit Framework payload for remote interaction and malicious code execution.
- **Windows services modification**: Techniques like T1543.003 on MITRE ATT&CK to execute malicious scripts.
- **Run keys modification**: Adding entries in the Registry or Startup Folder for persistent payload execution.

**Question:** What is the technique used to modify file time attributes to hide new or changed files?
**Answer:** Timestomping

**Question:** Name the malicious script planted by an attacker on a webserver to maintain access.
**Answer:** Web shell

## Task 7: Command & Control

After establishing persistence, the attacker opens a C2 (Command and Control) channel to remotely control the compromised system. 

- **C2 Beaconing**: Regular communication between the C2 server and malware.
- **Common C2 Channels**:
  - **HTTP/HTTPS**: Using port 80 and 443 to blend malicious traffic with legitimate traffic.
  - **DNS Tunneling**: Constant DNS requests to a server/domain owned by the attacker.

**Question:** What is the C2 communication where the victim makes regular DNS requests to an attacker's DNS server/domain?
**Answer:** DNS Tunneling

## Task 8: Actions on Objectives (Exfiltration)

Finally, the attacker achieves their goals, such as:
- Collecting user credentials
- Performing privilege escalation
- Conducting internal reconnaissance
- Lateral movement through the network
- Exfiltrating sensitive data
- Deleting backups and shadow copies

**Question:** What technology included in Microsoft Windows creates backup copies or snapshots of files or volumes?
**Answer:** Shadow Copy

## Task 9: Practice Analysis

**Real-World Scenario: Target Cyber-Attack (November 27, 2013)**

### Steps to Complete the Practical:
1. Add each item on the list in the correct Kill Chain entry form on the Static Site Lab:
   - Exploit public-facing application
   - Data from local system
   - PowerShell
   - Dynamic linker hijacking
   - Spearphishing attachment
   - Fallback channels
2. Use the ‘Check answers’ button to verify correctness.
   ![Cyber Kill Chain Diagram](https://github.com/Shruti1533/TryHackMe-Cyber-Kill-Chain/blob/main/cyber%20kill%20chain%20thm%20diagram.png)

**Flag:** `THM{7HR347_1N73L_12_4w35om3}`
