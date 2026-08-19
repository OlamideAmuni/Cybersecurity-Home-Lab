# Kali Linux

## Overview

Kali Linux is one of the primary machines in my cybersecurity home lab.

I created this virtual machine to provide a dedicated environment where I can safely practice cybersecurity concepts, tools and techniques without interacting with systems I do not have authorization to test.

The machine serves mainly as my security testing and analysis workstation.

---

## Why I Created the Virtual Machine

I wanted my cybersecurity learning to move beyond watching tutorials and reading about tools.

Instead of simply learning what Nmap, Wireshark, Burp Suite or other security tools are, I wanted an environment where I could actually use them against systems I intentionally placed inside my home lab.

Running Kali Linux as a virtual machine also allows me to:

- Keep my security tools isolated from my main operating system- Create an easily repeatable cybersecurity environment
- Connect Kali to other virtual machines in my lab
- Practice reconnaissance and enumeration
- Perform authorized penetration-testing exercises
- Analyze network traffic
- Practice security monitoring and investigation
- Experiment with different configurations without affecting my host system

The VM therefore acts as a controlled security workstation within my lab.

---

## Role in My Home Lab

The Kali Linux VM is primarily used for:

- Reconnaissance
- Network discovery
- Enumeration
- Network analysis
- Vulnerability assessment
- Web security testing
- Basic penetration testing
- Security research

For example, when working with vulnerable machines such as Kioptrix, Kali acts as the testing workstation while the vulnerable machine acts as the target.

```text
                 Home Lab Network

              ┌─────────────────┐
              │   Kali Linux    │
              │ Security Tester │
              └────────┬────────┘
                       │
                 Lab Network
                       │
          ┌────────────┼────────────┐
          │            │            │
          ▼            ▼            ▼
      Kioptrix     Windows 10   Ubuntu Server
       Target        Endpoint       Server

```

## Network Configuration
The Kali VM is connected to my isolated home-lab network (VMnet8, NAT) so that it can communicate with other virtual machines (which is connected  to the same networ NAT) used for testing.
The network configuration allows me to build scenarios where Kali can interact with vulnerable targets and defensive machines inside the lab.

---

## Tools I Used
- ping : to check connectivity in lab

  ping < target IP address>
- nmap : Identify targets,host,open port, OS and Service version.
  
  nmap -T4 -p < target IP address >
- netdiscover: to discover network host
- Google fu: to search for specific service version found for details
- metasploit: exploiting tool

---

## Lessons Learned
Building the Kali VM helped me move from theoretical cybersecurity learning toward practical experimentation.
One of the biggest lessons so far is that tools are only part of cybersecurity.
Knowing that Nmap exists is different from understanding:
- Why I am scanning
- What information I am looking for
- How to interpret the results
- What the results tell me about the target
- What I should investigate next.
  
The goal of this machine is therefore not simply to collect security tools,It is to develop the ability to observe, investigate, reason and validate
