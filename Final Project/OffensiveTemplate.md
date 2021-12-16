# Red Team: Summary of Operations

## Table of Contents
- Exposed Services
- Critical Vulnerabilities
- Exploitation

### Exposed Services
_TODO: Fill out the information below._

Nmap scan results for each machine reveal the below services and OS details:

```bash
$ nmap ... # TODO: Add command to Scan Target 1
  # $ nmap -sV 192.168.1.110
```
ELK machine 
IP Address: 192.168.1.100
Kali: 
IP Address: 192.168.1.90
Capstone: Filebeat and Metricbeat are installed and will forward logs to the ELK machine.
IP Address: 192.168.1.105
Target 1: Exposes a vulnerable WordPress server.
IP Address: 192.168.1.110


This scan identifies the services below as potential points of entry:
- Target 1
 
22 ssh
80 http
111 rpcbind
139 netbios-ssn
445 micrsoft-ds 

The following vulnerabilities were identified on each target:
- Target 1
 Wordpress user enumeration wpscan
weak password

_TODO: Include vulnerability scan results to prove the identified vulnerabilities._

### Exploitation
_TODO: Fill out the details below. Include screenshots where possible._

The Red Team was able to penetrate `Target 1` and retrieve the following confidential data:
- Target 1
  - `flag1.txt`: b9bbcb33e11b80be759c4e844862482
    - **Exploit Used**
      - _TODO: Identify the exploit used_
      - _TODO: Include the command run_
  - `flag2.txt`: _TODO: Insert `flag2.txt` hash value_
    - **Exploit Used**
      - _TODO: fc3fd58dcdad9ab23faca6e9a36e581c
      - _TODO: Include the command run_