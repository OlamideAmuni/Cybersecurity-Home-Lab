# Home Cybersecurity Lab

## Overview

This repository documents the design and development of my personal cybersecurity home lab built using VMware Workstation Pro. The objective of this lab is to create a realistic enterprise-like environment where multiple systems communicate over a virtual network for hands-on learning, experimentation, and security research.

The lab is designed to strengthen practical skills in network security, system administration, security monitoring, and Industrial Control Systems (ICS) security through real-world simulations rather than isolated virtual machines.

---

# Lab Architecture

The virtual machines are connected using VMware's **NAT Network (VMnet8)**.

Using a shared NAT network allows every virtual machine to communicate with one another while remaining isolated from the physical network(keeping the virtual Machines in the same  virtual private Subnet. This provides a safe environment for conducting cybersecurity experiments without affecting external devices.

This network design makes it possible to:

- Perform host discovery
- Practice network reconnaissance and enumeration
- Simulate communication between enterprise systems
- Generate realistic network traffic
- Build and test security monitoring solutions
- Safely perform offensive and defensive security exercises

---

# Virtual Machines

## Kali Linux

**Role:** Attacker / Security Testing Workstation

Kali Linux serves as the primary security assessment machine used for offensive security operations.

### Current Activities

- Network reconnaissance
- Host discovery
- Service enumeration
- Vulnerability assessment
- Penetration testing
- Python security tool development

---

## Windows 10

**Role:** Enterprise Workstation

The Windows 10 virtual machine represents a typical employee workstation found within an enterprise environment.

### Purpose

- Generate Windows security events
- Simulate normal user activities
- Serve as the monitored endpoint for security solutions
- Host OpenPLC Runtime for future ICS security experiments

This system will later be integrated with centralized security monitoring solutions for log collection and analysis.

---

## Ubuntu Desktop

**Role:** Security Monitoring Server

Ubuntu Desktop serves as the central monitoring system within the lab.

### Purpose

- Host security monitoring services
- Receive logs from monitored endpoints
- Act as the foundation for centralized security visibility
- Support future SOC-related experiments

As the lab grows, this machine will become the central point for monitoring, detection, and analysis.

---

# Why This Architecture?

A cybersecurity lab becomes significantly more valuable when multiple systems interact instead of operating independently.

By allowing these virtual machines to communicate across the same virtual network, I can simulate many real-world security scenarios, including:

- Network scanning
- Service discovery
- Security monitoring
- Host communication analysis
- Threat detection
- Incident investigation

This architecture provides practical experience that closely resembles modern enterprise environments.

---

# Technologies

Current technologies used within the lab include:

- VMware Workstation Pro
- Kali Linux
- Windows 10
- Ubuntu Desktop
- OpenPLC Runtime
- Python
- Nmap
- Netdiscover

---

# Current Focus

This repository currently focuses on documenting the lab architecture and networking design.

Future updates will document the implementation of additional technologies and configurations, including:

- Sysmon deployment
- Splunk Cloud integration
- Splunk Universal Forwarder configuration
- Log collection and analysis
- Detection engineering
- Additional OT/ICS security components

---

# Project Status

> 🚧 **This repository is currently under active development.**

The home lab is continuously evolving as further configurations are needed to completely simulate SOC , Pentesting  and ICS environment.

Future updates will include:

- Security monitoring configurations(sysmon, Splunk)
- Additional virtual machines
- OT/ICS security simulations (OpenPLC, ScadaBR)

---

# Author

## Olamide Ridwan

**Mechatronics Engineering Student**

### Areas of Interest

- Cybersecurity
- Operational Technology (OT)
- Industrial Control Systems (ICS)
- Python Security Automation
