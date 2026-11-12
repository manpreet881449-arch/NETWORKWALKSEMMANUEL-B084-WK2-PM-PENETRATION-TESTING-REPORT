**PENETRATION TESTING REPORT Footprinting, Reconnaissance & Network Scanning Phases**

**W2-PM-FINAL | CYBERSECURITY | NETWORKWALKS**

**Field**                               	**Detail**

**Pentester Name (Cybersecurity Professional)** =	Manpreet Singh

**Program / Batch	B084**  =  Networkwalks

**Date**	             =  10 November 2026

**Modules completed**	 =  W2-PM1: Multiple Kali Tools
                         # W2-PM-FINAL – Cybersecurity 
                         # Ethical Hacking Practical Report

## Report Note

This document provides the main project overview for the five practical modules represented in this GitHub repository.

It summarizes the activities performed during PM1–PM5, including Kali Linux tool familiarization, GHDB footprinting, Maltego footprinting, theHarvester information gathering, and Nmap network scanning.

The report distinguishes between completed activities, observed results, and attempted tests. It does not claim that exploitation, vulnerability validation, or remediation testing was performed.

## 1. Liability Disclaimer

These materials document cybersecurity learning and practical exercises.

All testing of systems and networks must remain within an explicitly authorized scope. Public availability of a domain, website, hostname, or network service does not automatically grant permission to perform active security testing.

Passive information gathering and active network scanning are different activities and must be treated accordingly.

Do not use the techniques documented here to access, disrupt, exploit, or collect information from systems without appropriate authorization.

The student is responsible for following applicable laws, organizational policies, and instructor directions.

This public repository intentionally excludes sensitive information, including:

- Personal and employee-related information.
- Raw reconnaissance and collection output.
- Private IP addresses.
- MAC addresses.
- Internal gateway and routing details.
- Local network configuration information.
- Other potentially sensitive assessment data.

## 2. Introduction

This report covers my Week 2 Cybersecurity & Ethical Hacking practical work across five modules, W2-PM1 to W2-PM5.

The project introduces different reconnaissance, footprinting, information-gathering, and network-discovery techniques using Kali Linux security tools.

The five practical modules cover:

1. PM1 – Multiple Kali Linux Tools.
2. PM2 – Google Hacking Database (GHDB) Footprinting.
3. PM3 – Maltego Footprinting.
4. PM4 – theHarvester Footprinting.
5. PM5 – Network Scanning Using Nmap and Zenmap.

The purpose of these activities was to understand how cybersecurity professionals gather publicly available information, examine domain-related data, explore relationships between entities, and identify hosts and open network ports.

The project also emphasizes responsible testing, accurate reporting, validation of tool output, and protection of sensitive information.

## 3. Tools and Technologies Used

| Module | Tool / Technology | Purpose |
|---|---|---|
| PM1 | WHOIS | Domain registration information lookup |
| PM1 | WhatWeb | Website technology identification |
| PM1 | nslookup | DNS information lookup |
| PM1 | curl | HTTP requests and response inspection |
| PM1 | wafw00f | Web application firewall identification |
| PM1 | dnsrecon | DNS reconnaissance |
| PM2 | Google Hacking Database (GHDB) | Search-based footprinting |
| PM3 | Maltego | Visual footprinting and relationship analysis |
| PM4 | theHarvester 4.11.1 | OSINT and domain-related information gathering |
| PM5 | Nmap 7.99.1 | Network discovery and port scanning |
| PM5 | Zenmap | Graphical interface for Nmap |

**Operating System:** Kali Linux.

## 4. Activities Performed

### 4.1 PM1 – Multiple Kali Linux Tools

**Project Folder:** `PM1-Multiple-Kali-Tools/`

For PM1, I worked with multiple tools available in Kali Linux as part of the assigned cybersecurity practical exercises.

**Tools used:**

- WHOIS
- WhatWeb
- nslookup
- curl
- wafw00f
- dnsrecon

**Objectives:**

- Understand commonly used Kali Linux reconnaissance tools.
- Practice domain and DNS information gathering.
- Examine website technologies and HTTP responses.
- Understand the purpose of web application firewall detection.
- Become familiar with DNS reconnaissance techniques.

This module provided introductory practical exposure to different command-line tools used during reconnaissance and footprinting.

### 4.2 PM2 – GHDB Footprinting

**Project Folder:** `PM2-GHDB-Footprinting/`

For PM2, I performed search-based footprinting exercises using the Google Hacking Database (GHDB).

**Objectives:**

- Understand the purpose of Google search operators in cybersecurity.
- Learn how search queries can identify publicly indexed information.
- Explore the use of advanced search operators.
- Understand how publicly indexed information may contribute to reconnaissance.
- Review search results responsibly and within the approved scope.

GHDB-based footprinting is an information-gathering technique. A search result does not automatically establish that a website or system is vulnerable.

### 4.3 PM3 – Maltego Footprinting

**Project Folder:** `PM3-Maltego-Footprinting/`

For PM3, I used Maltego to practice visual footprinting and examine relationships between entities.

**Objectives:**

- Understand visual reconnaissance.
- Explore entity-based information gathering.
- Examine relationships represented through Maltego transforms.
- Understand how related information can be organized into a visual graph.
- Review collected information and its relevance to footprinting.

Maltego helps organize information into connected entities and relationships. These relationships require independent verification before being treated as confirmed findings.

### 4.4 PM4 – theHarvester Footprinting

**Project Folder:** `PM4-theHarvester/`  
**Public Documentation:** `PM4-theHarvester/reports/README.md`

For PM4, I used theHarvester version 4.11.1 on Kali Linux to perform domain-related OSINT information gathering.

**Activities performed:**

- Displayed theHarvester help information and reviewed its available options.
- Explored supported OSINT information sources.
- Executed a Baidu-based search for `microsoft.com`.
- Reviewed the returned hostname information.
- Attempted additional information gathering against `google.com`.
- Reviewed provider responses and observed source-related warnings.
- Saved command output locally for analysis.
- Prepared sanitized documentation for public GitHub publication.

**Confirmed Microsoft/Baidu observation:**

- Hostnames reported: 6.
- IP addresses reported: 0.
- Email addresses reported: 0.
- People-related records reported: 0.

Additional Google/HudsonRock testing returned zero hosts, IP addresses, email addresses, and stealer records, with response-format warnings observed.

Other Google/Baidu and all-source commands were also included in the testing process. Their results are documented only when supported by their actual execution output.

**Data protection:**

Raw collection output, employee-related information, email addresses, and potentially sensitive hostname information are excluded from the public repository.

### 4.5 PM5 – Network Scanning Using Nmap and Zenmap

**Project Folder:** `PM5-Network-Scanning/`  
**Public Documentation:** `PM5-Network-Scanning/reports/README.md`

For PM5, I practiced network discovery and scanning using Nmap and its graphical interface, Zenmap.

The practical evidence includes two distinct scanning activities.

**Activity A – Lab Network Host Discovery**

Scan type: Ping Scan / Host Discovery (`-sn`).

Recorded results:

- Total addresses scanned: 256.
- Hosts reported up: 4.

Objective:

- Identify active hosts in the lab network.
- Understand basic host discovery.
- Review network discovery output.
- Document the scan summary without publishing local network identifiers.

**Activity B – Zenmap Intense Scan**

The supplied Zenmap screenshot documents an Intense Scan against `google.com`.

Configuration:

- Tool: Zenmap.
- Nmap version: 7.99.1.
- Profile: Intense Scan.
- Command: `nmap -T4 -A -v google.com`.
- TCP ports scanned: 1,000.
- Target IP selected by Nmap: documented in the local evidence, excluded from this public summary.

Observed results:

- TCP port 80 was reported open.
- TCP port 443 was reported open.
- Service detection was initiated.
- OS detection was attempted.
- Traceroute was initiated.
- NSE scripts were loaded.

The supplied screenshot shows intermediate scan output rather than the complete final report.

**Important distinction:**

The 256-address Ping Scan and the Google Intense Scan are separate activities. The open-port results from the Intense Scan must not be presented as findings from the lab host-discovery scan.

The Zenmap screenshot does not establish a vulnerability or successful exploitation.

**Data protection:**

Private IP addresses, MAC addresses, gateway details, routing information, and raw local network scan files are excluded from this public repository.

## 5. Risk Analysis and Security Observations

The following table describes general security considerations associated with the activities performed. These are not confirmed vulnerabilities.

| No. | Observation | Potential Impact | General Risk Consideration |
|---|---|---|---|
| 1 | Publicly indexed information discovered through footprinting | May help build an initial profile of an organization | Low–Medium |
| 2 | Relationships identified through visual footprinting | May reveal connections between publicly available entities | Low–Medium |
| 3 | Domain-related information returned by theHarvester | May provide additional context about an organization's public footprint | Low–Medium |
| 4 | Active hosts identified in a lab network | Unknown or unmanaged devices may increase the network attack surface | Medium |
| 5 | Open HTTP and HTTPS ports observed during the Intense Scan | Indicates accessible web services that may require routine security review | Informational |

**Risk rating note:**

These are general observations, not confirmed risk ratings for the target systems.

A formal risk rating requires asset ownership and context, verification of findings, vulnerability analysis, and an assessment of likelihood and impact.

Open ports, public information, and responding hosts do not independently establish the presence of vulnerabilities.

## 6. Recommendations

Based on the learning outcomes of these practical activities, the following general security practices are recommended:

1. **Define authorized scope:** Confirm approved domains, IP ranges, systems, testing windows, and permitted tools before conducting assessments.
2. **Review public information:** Periodically review organizational information exposed through search engines and public sources.
3. **Validate tool output:** Cross-check results and distinguish confirmed observations from warnings, incomplete responses, and false positives.
4. **Protect personal information:** Avoid publishing harvested personal information, employee details, or email addresses.
5. **Review entity relationships:** Independently verify relationships identified through visual footprinting.
6. **Maintain an asset inventory:** Compare discovered lab hosts with approved network documentation.
7. **Keep systems updated:** Review operating systems, applications, and services against relevant security advisories.
8. **Review exposed services:** Ensure that publicly accessible services are necessary, properly configured, and maintained.
9. **Protect network information:** Remove private IP addresses, MAC addresses, gateway details, and internal configuration information from public reports.
10. **Document findings accurately:** Record the objective, tool, scope, observed results, limitations, and recommended actions.
11. **Perform further testing only with permission:** Vulnerability validation and exploitation require explicit authorization and a defined testing scope.

## 7. Conclusion

During Week 2 of my Cybersecurity & Ethical Hacking practical program, I worked on five modules covering Kali Linux tools, GHDB footprinting, Maltego footprinting, theHarvester information gathering, and Nmap network scanning.

These exercises provided practical exposure to different reconnaissance and information-gathering approaches.

I learned how to use multiple Kali Linux tools, explore search-based footprinting, examine entity relationships, collect domain-related information using theHarvester, and identify hosts and open ports using Nmap and Zenmap.

The practical work also highlighted the importance of validating tool output, understanding scanning limitations, documenting observations accurately, protecting sensitive information, and maintaining an authorized testing scope.

These five modules provided a foundation for understanding reconnaissance and network discovery as part of a broader cybersecurity assessment workflow.

No exploitation or confirmed vulnerability validation is claimed in this report.

## 8. Evidence and Project Files

The project is organized into five module folders:

| Module | Project Folder | Documentation |
|---|---|---|
| PM1 – Multiple Kali Tools | `PM1-Multiple-Kali-Tools/` | Module practical material |
| PM2 – GHDB Footprinting | `PM2-GHDB-Footprinting/` | Module practical material |
| PM3 – Maltego Footprinting | `PM3-Maltego-Footprinting/` | Module practical material |
| PM4 – theHarvester Footprinting | `PM4-theHarvester/` | `reports/README.md` |
| PM5 – Network Scanning | `PM5-Network-Scanning/` | `reports/README.md` |

### Repository Structure

```text
W2-PM-FINAL/
│W2-PM-FINAL/
│
├── README.md
│
├── PM1-Multiple-Kali-Tools/
│   ├── outputs/
│   └── screenshots/
│
├── PM2-GHDB-Footprinting/
│   ├── outputs/
│
├── PM3-Maltego-Footprinting/
│   ├── outputs/
│   └── screenshots/
│
├── PM4-theHarvester/
│   ├── reports/
│   │   └── README.md
│   ├── outputs/
│   └── screenshots/
│
└── PM5-Network-Scanning/
    ├── reports/
    │   └── README.md
    ├── outputs/
    └── screenshots/

```

**Evidence note:** The structure above describes the intended organization. Only files actually committed to the repository should be represented as published evidence. Local raw output and sensitive screenshots should remain excluded from public uploads.

Screenshots should be added only after confirming that they are original, belong to the respective practical module, and do not disclose sensitive information.

---

**End of Report**

**W2-PM-FINAL | Cybersecurity & Ethical Hacking | Networkwalks | PM1–PM5**
                      W2-PM2: GHDB Footprinting
                      W2-PM3: Maltego Footprinting
                      W2-PM4: theHarvester Footprinting
                      W2-PM5: Network Scanning

Testing environment =	Kali Linux and an authorized lab environment

Phases covered	    =  Phase 1: Reconnaissance & Footprinting
                       Phase 2: Information Gathering & Analysis
                       Phase 3: Network Scanning & Host Discovery






