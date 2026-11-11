# PM5 – Network Scanning Using Nmap and Zenmap

## 1. Project Overview

**Project Name:** PM5 – Network Scanning  
**Module:** Week 2 – Cybersecurity Project  
**Category:** Network Reconnaissance and Scanning  
**Tool:** Zenmap (Nmap GUI)  
**Nmap Version:** 7.99.1  
**Operating System:** Kali Linux  
**Target Domain:** google.com

## 2. Objective

The objective of this practical exercise is to understand network scanning and host discovery using Nmap through its graphical interface, Zenmap.

The exercise demonstrates how security professionals can identify accessible network services, discover open ports, perform service detection, and understand the basic reconnaissance process.

The practical also introduces different Nmap scanning techniques and their purposes in network security assessments.

## 3. Tools and Technologies

| Tool / Technology | Purpose |
|---|---|
| Kali Linux | Security testing environment |
| Zenmap | Graphical interface for Nmap |
| Nmap 7.99.1 | Network scanning engine |
| TCP SYN Scan | Identify open TCP ports |
| NSE | Nmap Scripting Engine |
| DNS Resolution | Resolve domain names to IP addresses |

## 4. Introduction to Nmap

Nmap (Network Mapper) is an open-source network discovery and security auditing tool.

It is commonly used by network administrators and cybersecurity professionals to:

- Discover active hosts.
- Identify open, closed, and filtered ports.
- Detect running network services.
- Identify service versions.
- Attempt operating system detection.
- Perform network reconnaissance.
- Execute selected security checks through NSE scripts.

Nmap is an important tool during the reconnaissance and network enumeration phases of a penetration testing assessment.

## 5. Introduction to Zenmap

Zenmap is the graphical user interface (GUI) for Nmap.

It allows users to configure scan targets, select scanning profiles, execute scans, and review results without entering every command manually.

Important Zenmap features include:

- Target configuration.
- Predefined scanning profiles.
- Custom Nmap commands.
- Nmap output visualization.
- Port and host information.
- Network topology visualization.
- Scan history.

## 6. Scan Configuration

The attached practical screenshot shows the following configuration:

| Configuration | Value |
|---|---|
| Target | google.com |
| Profile | Intense Scan |
| Command | `nmap -T4 -A -v google.com` |
| Nmap Version | 7.99.1 |
| Selected Target IP | 142.250.122.102 |

**Important:** This screenshot documents an Intense Scan, not a Ping Scan (`-sn`).

## 7. Command Execution and Explanation

### Command Used

```bash
nmap -T4 -A -v google.com
```

This is the command displayed in the Zenmap screenshot.

### Command Breakdown

**1. `nmap`**

Executes the Nmap network scanning utility.

**2. `-T4` – Timing Template**

Sets the scanning speed to timing template 4 (Aggressive).

It helps speed up scanning but may generate more network traffic.

**3. `-A` – Aggressive Scan Options**

Enables several advanced detection features, including:

- Operating system detection.
- Service and version detection.
- Default NSE script scanning.
- Traceroute.

**4. `-v` – Verbose Mode**

Displays additional information about the scanning process.

It helps the user observe scanning activities and progress.

## 8. Understanding the Scan Process

Based on the attached screenshot, the following scanning stages were visible.

### Stage 1: Nmap Initialization

Nmap 7.99.1 started successfully.

The output also indicated that 158 NSE scripts were loaded for scanning.

### Stage 2: DNS Resolution

Nmap performed DNS resolution for the target domain.

The output showed:

```text
Hostname google.com resolves to 10 IPs.
Using 142.250.122.102.
```

This indicates that the domain resolved to multiple IP addresses, while Nmap selected one address for the displayed scan.

### Stage 3: Ping Scan

Nmap initiated its initial host discovery stage.

The screenshot showed:

```text
Scanning google.com (142.250.122.102) [4 ports]
```

This was part of Nmap's host discovery process within the selected Intense Scan profile.

It should not be confused with the standalone `-sn` scan option.

### Stage 4: TCP SYN Stealth Scan

Nmap initiated a SYN scan against 1000 TCP ports.

The screenshot displayed:

```text
Initiating SYN Stealth Scan
Scanning google.com (142.250.122.102) [1000 ports]
```

A SYN scan sends TCP SYN packets to identify the state of ports without completing a full TCP connection in the usual open-port case.

### Stage 5: Open Port Discovery

The following two open ports were identified:

```text
Discovered open port 80/tcp
Discovered open port 443/tcp
```

**Port 80 – HTTP**

Port 80 is commonly used for HTTP communication between web clients and servers.

**Port 443 – HTTPS**

Port 443 is commonly used for HTTPS communication, which provides encrypted web communication using TLS.

An open port indicates that a service is accepting connections at the time of scanning. It does not automatically indicate a security vulnerability.

### Stage 6: Service Detection

Nmap initiated service detection for the two discovered open ports.

The screenshot displayed:

```text
Initiating Service scan
Scanning 2 services on google.com
```

Service detection attempts to identify which applications or services are listening on the discovered ports.

The final service names and versions are not visible in the supplied screenshot.

### Stage 7: Operating System Detection

Nmap initiated operating system detection.

The screenshot showed multiple OS detection attempts.

This feature attempts to estimate the operating system based on network response characteristics.

No confirmed operating system identification is visible in the supplied evidence.

### Stage 8: Traceroute

Nmap initiated traceroute.

Traceroute helps identify network hops between the scanning system and the target.

The screenshot confirms that traceroute was initiated, but does not show its complete final route.

### Stage 9: NSE Script Scanning

Nmap also initiated NSE script scanning.

NSE (Nmap Scripting Engine) allows Nmap to perform additional network discovery and service-related checks using scripts.

The screenshot confirms that 158 scripts were loaded, but does not establish that all 158 scripts executed against the target.

## 9. Scan Results

### Observed Findings

| Finding | Result |
|---|---|
| Target domain | google.com |
| Resolved IPs | 10 reported |
| IP selected for scan | 142.250.122.102 |
| TCP ports scanned | 1000 |
| Open TCP ports observed | 2 |
| Port 80 | Open |
| Port 443 | Open |
| Service detection | Initiated |
| OS detection | Attempted |
| Traceroute | Initiated |
| NSE scripts loaded | 158 |

### Key Observations

1. Nmap successfully started and resolved the target domain.
2. The domain returned multiple IP addresses.
3. One IP address was selected for the displayed scan.
4. Nmap initiated a SYN scan against 1000 TCP ports.
5. Ports 80 and 443 were identified as open.
6. Service detection was initiated for the two open ports.
7. OS detection, traceroute, and NSE scanning activities were also initiated.
8. The supplied screenshot contains intermediate scan output, not the complete final report.

## 10. Understanding Different Nmap Scan Types

| Scan Type | Command | Purpose |
|---|---|---|
| Ping Scan | `nmap -sn` | Host discovery without a port scan |
| SYN Scan | `nmap -sS` | Identify TCP port states |
| TCP Connect Scan | `nmap -sT` | Complete TCP connection-based scanning |
| Service Detection | `nmap -sV` | Identify services and versions |
| OS Detection | `nmap -O` | Attempt operating system identification |
| Intense Scan | `nmap -T4 -A -v` | Combine multiple scanning and detection features |

These commands should only be executed against systems for which testing permission has been obtained.

## 11. Limitations

- Scan results represent the network conditions at the time of testing.
- DNS may resolve a domain to multiple IP addresses.
- Different IP addresses may return different results.
- Firewalls and filtering systems may affect scan results.
- Service detection may not always identify exact application versions.
- OS detection is an estimate and is not always accurate.
- A screenshot of intermediate output cannot establish the complete final scan result.
- Open ports do not automatically indicate vulnerabilities.

## 12. Security and Ethical Considerations

Network scanning should always be conducted within an authorized testing scope.

This practical uses a publicly accessible domain as the target shown in the screenshot. Public accessibility does not mean that unrestricted security scanning is authorized.

For future exercises, use an intentionally vulnerable virtual machine, an isolated lab network, or another system for which explicit permission has been granted.

No exploitation or vulnerability confirmation is established by this screenshot.

## 13. Data Protection

The public repository should contain only non-sensitive project documentation and approved screenshots.

The following information should be excluded from public uploads where it could reveal private infrastructure:

- Private IP addresses.
- MAC addresses.
- Internal gateway details.
- Private network topology.
- Raw scan output files.
- Sensitive host and service information.

## 14. Conclusion

This practical exercise introduced network scanning using Zenmap and the Nmap scanning engine.

The attached screenshot demonstrates the execution of an Intense Scan against google.com using Nmap 7.99.1.

The scan output showed that the selected target IP address was 142.250.122.102 and that TCP ports 80 and 443 were identified as open among the 1000 ports scanned.

The exercise also demonstrated DNS resolution, TCP SYN scanning, service detection, OS detection attempts, traceroute initiation, and the use of NSE scripts.

Overall, this practical improved understanding of network reconnaissance, port discovery, and the role of Nmap in cybersecurity assessments.

## 15. Evidence and Repository Structure

```text
PM5-Network-Scanning/
│
├── README.md
│
├── screenshots/
│   ├── 01-zenmap-scan-configuration.png
│   └── 02-nmap-intense-scan-output.png
│
└── outputs/
    └── (Excluded from public repository)
```

**Evidence note:** The screenshot supplied for this practical documents the Intense Scan configuration and intermediate Nmap output. A separate authorized lab Ping Scan screenshot should be added if the assignment specifically requires the `-sn` host discovery exercise.
