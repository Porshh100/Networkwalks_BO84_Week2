# Networkwalks_BO84_Week2

Week 2 cybersecurity report: Kali Linux footprinting and Zenmap network scanning.

![Kali Linux](https://img.shields.io/badge/Kali-Linux-557C94?logo=kalilinux&logoColor=white)
![Nmap](https://img.shields.io/badge/Nmap-Zenmap-4682B4)
![Cybersecurity](https://img.shields.io/badge/Cybersecurity-Ethical%20Hacking-red)
![Networkwalks](https://img.shields.io/badge/Networkwalks-Week%202-darkred)

**W2-PM FINAL | CYBERSECURITY & ETHICAL HACKING | NETWORKWALKS**

# Cybersecurity Reconnaissance & Information Gathering

## Project Overview

This repository documents practical cybersecurity reconnaissance activities performed using Kali Linux and Windows. The exercises focused on understanding how security professionals gather information about targets, identify network assets, discover live hosts, and analyse publicly available information during the early stages of a security assessment.

The practical tasks provided hands-on exposure to reconnaissance tools and network discovery techniques commonly used in cybersecurity and penetration testing.

## Objectives

- Understand the reconnaissance phase of cybersecurity assessments.
- Perform passive information gathering using OSINT tools.
- Identify publicly available information about a target domain.
- Discover active devices on a local network.
- Identify IP addresses and MAC addresses of discovered hosts.
- Understand network mapping and topology visualisation.
- Gain practical experience with command-line and graphical reconnaissance tools.

## Tools & Technologies Used

| Tool | Purpose |
|---|---|
| Kali Linux | Security testing environment |
| theHarvester | OSINT and information gathering |
| Nmap | Network discovery and scanning |
| Zenmap | Graphical interface for Nmap |
| Windows CMD | Network information and ARP table inspection |
| VirtualBox | Virtualisation environment |

---

## Task 1: Passive Reconnaissance Using theHarvester

**Tool:** theHarvester

**Objective:** Gather publicly available information associated with a target domain.

theHarvester is an OSINT (Open-Source Intelligence) tool used to collect information such as email addresses, hostnames, IP addresses, employee names and other publicly indexed information.

### Command Executed

```bash
theHarvester -d microsoft.com -l 50 -b all
```

### Command Breakdown

- `theHarvester`: Launches the information-gathering tool.
- `-d microsoft.com`: Specifies the target domain.
- `-l 50`: Sets the maximum result limit to 50.
- `-b all`: Attempts to use all supported data sources.

### Observations and Findings

During execution, the tool attempted to retrieve publicly available information from multiple search engines and data providers.

The results indicated:

- No email addresses were successfully retrieved.
- No employee names were successfully identified.
- No hostnames or IP addresses were returned in the displayed results.
- Some data providers required API keys.
- Certain sources experienced errors or timeouts.
- Hudson Rock returned zero hosts, IP addresses and emails.

**Learning Outcome:**

I gained practical exposure to OSINT reconnaissance, domain-based information gathering, and the importance of understanding external data-source limitations when conducting information-gathering exercises.

---

## Task 2: Network Reconnaissance Using Nmap

**Tool:** Nmap

**Objective:** Understand network discovery and identify active hosts within a local network.

Nmap (Network Mapper) is a network discovery and security auditing tool used to identify devices, discover open ports and investigate network services.

### Network Discovery Command

```bash
nmap -sn 192.168.0.0/24
```

### Command Breakdown

- `nmap`: Launches the Nmap scanning tool.
- `-sn`: Performs host discovery without conducting a port scan.
- `192.168.0.0/24`: Specifies the local network subnet.

**Purpose:**

The scan is designed to identify devices that respond to Nmap's host-discovery probes within the specified subnet.

---

## Task 3: Network Discovery Using Zenmap

**Tool:** Zenmap

**Objective:** Perform network discovery through a graphical interface and identify live hosts on the local network.

Zenmap provides a graphical interface for Nmap, making it easier to configure scans, review results and visualise network relationships.

### Network Configuration

The recorded Windows network configuration was:

| Network Detail | Value |
|---|---|
| Local IPv4 Address | 192.168.0.239 |
| Subnet Mask | 255.255.255.0 |
| Default Gateway | 192.168.0.1 |
| LAN Subnet | 192.168.0.0/24 |

### Scanning Procedure

1. Opened Zenmap on Windows.
2. Entered the local network subnet into the Target field.
3. Selected the Ping Scan profile.
4. Initiated the network discovery scan.
5. Reviewed the Nmap output to identify active hosts.

### Scan Configuration

```text
Target: 192.168.0.0/24
Profile: Ping Scan
```

### Information to Record

- List of discovered live hosts.
- Total number of active hosts.
- IP addresses of discovered devices.
- MAC addresses of discovered devices.

**Note:** The actual host-discovery results must be added after completing and saving the Zenmap scan.

---

## Task 4: MAC Address Identification

**Tool:** Windows Command Prompt

**Objective:** Identify the MAC addresses associated with discovered network devices.

A MAC (Media Access Control) address is a hardware address associated with a network interface.

### Command Used

```cmd
arp -a
```

### Purpose

The ARP table displays IP-to-MAC address mappings that the computer has learned through Address Resolution Protocol.

This information can help associate discovered IP addresses with their corresponding MAC addresses.

**Information to Record:**

| IP Address | MAC Address |
|---|---|
| To be completed | To be completed |
| To be completed | To be completed |

---

## Task 5: Network Topology Mapping

**Tool:** Zenmap

**Objective:** Visualise discovered network devices and their relationships through a network topology diagram.

Zenmap includes a Topology tab that provides a graphical representation of discovered hosts and network relationships.

### Procedure

1. Completed the network discovery scan.
2. Opened the Topology tab.
3. Reviewed the discovered network devices.
4. Generated a graphical network representation.
5. Saved the topology output in PDF format.

**Expected Deliverable:**

`network_topology.pdf`

The topology PDF should be added to the repository or linked as a separate project attachment once exported.

---

## Skills & Knowledge Gained

Through these practical exercises, I developed an understanding of:

- Passive reconnaissance and OSINT.
- Domain information gathering.
- Using theHarvester for publicly available intelligence.
- Network discovery using Nmap.
- Configuring scans through Zenmap.
- Understanding IPv4 addresses and subnet masks.
- Identifying live network hosts.
- Understanding IP-to-MAC address mapping.
- Network topology visualisation.
- Interpreting reconnaissance tool output.
- Recognising API limitations and unsuccessful data-source queries.

## Conclusion

These exercises strengthened my understanding of the reconnaissance and information-gathering phase of cybersecurity assessments.

I gained hands-on experience with industry-relevant tools, including theHarvester, Nmap and Zenmap, while learning how publicly available information and network discovery techniques contribute to understanding an organisation's digital and network footprint.

Reconnaissance is an important foundation for identifying potential exposure, understanding network environments and supporting subsequent security assessment activities.

---

**Disclaimer:** All reconnaissance activities should be conducted for authorised educational, research or security assessment purposes. Information gathering and network scanning must comply with applicable laws and the target owner's permission.
