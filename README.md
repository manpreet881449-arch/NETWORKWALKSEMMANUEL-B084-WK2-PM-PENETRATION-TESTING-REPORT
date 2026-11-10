PENETRATION TESTING REPORT
Footprinting, Reconnaissance & Network Scanning Phases

W2-PM-FINAL | CYBERSECURITY | NETWORKWALKS
Field	Detail

Pentester Name (Cybersecurity Professional)	Manpreet Singh
Program / Batch	B084 – Networkwalks
Date	10 November 2026
Modules completed	W2-PM1: Multiple Kali Tools
W2-PM2: GHDB Footprinting
W2-PM3: Maltego Footprinting
W2-PM4: theHarvester Footprinting
W2-PM5: Network Scanning
Testing environment	Kali Linux and an authorized lab environment
Phases covered	Phase 1: Reconnaissance & Footprinting
Phase 2: Information Gathering & Analysis
Phase 3: Network Scanning & Host Discovery


Report note: This is the main project overview for the five modules currently represented in this GitHub repository. It describes the work at a summary level and does not claim that exploitation or vulnerability validation was performed.

1. Liability Disclaimer

I have performed these activities for educational purposes and within systems, domains and networks that I own or have been authorized to assess. All materials are intended for cybersecurity learning and research only.

Do not use these techniques to access, disrupt or collect information from systems without permission. The student is responsible for ensuring that all activities remain within the approved scope and comply with applicable laws, policies and instructor directions.

This public repository intentionally excludes sensitive information such as personal data, raw collection output, private IP addresses, MAC addresses, gateway details and other local network information.

2. Introduction

This report covers my Week 2 Cybersecurity & Ethical Hacking practical work across five modules, W2-PM1 to W2-PM5.

The project includes practical exercises using multiple Kali Linux tools, Google Hacking Database (GHDB) footprinting, Maltego footprinting, theHarvester information gathering and Nmap network scanning.

The purpose of these activities was to understand how cybersecurity professionals perform reconnaissance, gather and review information from different sources, examine relationships between entities, and identify live hosts in an authorized lab network.

The work is organized into five module folders in this GitHub repository. The PM4 and PM5 folders currently include sanitized public summary reports. Raw output and potentially sensitive evidence have not been published.

3. Tools Used

The following tools and platforms are represented in the five modules.
Tool	Purpose
Kali Linux	Operating system used for cybersecurity practical exercises
Multiple Kali Linux tools	Perform the assigned tool-based practical activities in PM1
Google Hacking Database (GHDB)	Learn search-based footprinting techniques in PM2
Maltego	Perform visual footprinting and examine relationships between entities in PM3
theHarvester	Gather domain-related information from supported sources in PM4
Nmap	Perform network host discovery in PM5

4. Activities Performed
4.1 PM1 – Multiple Kali Tools
For PM1, I worked with multiple tools available in Kali Linux as part of the assigned cybersecurity practical exercises.

Objective:
- Become familiar with Kali Linux tools used in cybersecurity activities.
- Practice the assigned tool-based tasks.
- Organize the practical work and supporting material.
Project folder: PM1-Multiple-Kali-Tools/

The folder contains the PM1 project material committed to this repository.
4.2 PM2 – GHDB Footprinting
For PM2, I completed the assigned footprinting activities using the Google Hacking Database (GHDB).

Objective:
- Understand search-based footprinting.
- Explore how GHDB search operators can identify information indexed by search engines.
- Review results carefully and keep activities within the approved scope.
Project folder: PM2-GHDB-Footprinting/
4.3 PM3 – Maltego Footprinting
For PM3, I used Maltego for the assigned footprinting and information-gathering exercise.

Objective:
- Practice visual footprinting.
- Examine relationships between entities and information represented in Maltego.
- Organize the practical work for review.
Project folder: PM3-Maltego-Footprinting/
4.4 PM4 – theHarvester Footprinting
For PM4, I used theHarvester to perform domain-related information gathering and reviewed the output returned by the selected sources.

Tool used: theHarvester

Activities performed:
- Ran theHarvester as part of the assigned footprinting tasks.
- Reviewed the collected output and source responses.
- Observed that some sources returned response-format warnings.
- Prepared a sanitized public summary for the repository.
Project documentation: PM4-theHarvester/reports/README.md

Raw collection output, personal information, employee-related information and potentially sensitive host data are intentionally excluded from this public repository.

4.5 PM5 – Network Scanning

For PM5, I used Nmap to perform ping-scan host discovery in a lab network.

Tool used: Nmap

Scan type: Ping Scan / Host Discovery (-sn)

Recorded scan summary:
- Addresses scanned: 256
- Hosts reported up: 4
Activities performed:
- Performed host discovery in the lab network.
- Reviewed the scan summary.
- Prepared a sanitized public report without publishing local network identifiers.
Project documentation: PM5-Network-Scanning/reports/README.md

Private IP addresses, MAC addresses, gateway information, routing details and raw scan files are intentionally excluded from this public repository.

5. Risk Analysis / Impact

The activities demonstrate how information gathered during footprinting and network discovery may be useful during an authorized security assessment. The observations below describe potential security considerations; they are not confirmed vulnerabilities.
#	Risk / Observation	Potential Impact	Risk Level
1	Publicly indexed information discovered during footprinting	May help build an initial profile of an organization or domain	Low–Medium
2	Relationships identified during visual footprinting	May help an assessor understand connections between publicly available entities	Low–Medium
3	Domain-related information returned by theHarvester	May provide additional context about a domain's public footprint	Low–Medium
4	Live hosts identified during network discovery	Unexpected or unmanaged devices may increase the network attack surface	Medium


Risk level note: These are general considerations based on the type of activity performed. A confirmed risk rating requires asset context, validation and an assessment of likelihood and impact.

The practical exercises primarily involved footprinting, information gathering and host discovery. No exploitation or vulnerability validation is claimed in this report. The presence of publicly available information or a responding host does not, by itself, prove that a system is vulnerable.

6. Recommendations

Based on the learning outcomes of these activities, I recommend the following general security practices:
1. Define the authorized scope: Confirm the approved domains, IP ranges, systems, testing window and permitted tools before beginning any assessment.
2. Review public information: Periodically review what organizational information is publicly indexed and remove information that should not be exposed.
3. Validate tool output: Cross-check results and distinguish confirmed observations from warnings, incomplete responses or false positives.
4. Protect personal information: Do not publish harvested personal data, employee details, email addresses or raw hostname lists in public repositories.
5. Review discovered relationships: Verify that footprinting results are relevant and accurate before drawing security conclusions.
6. Maintain an asset inventory: Compare discovered hosts with approved network documentation and investigate unknown devices.
7. Keep systems updated: Review operating systems, web applications and plugins against relevant security advisories.
8. Protect network details: Remove private IP addresses, MAC addresses, gateway information and local configuration details before publishing reports.
9. Document findings clearly: Record the objective, tool, authorized scope, observation, limitations and recommended action.
10. Perform further testing only with permission: Vulnerability validation and exploitation require explicit authorization and a defined scope.

7. Conclusion

During Week 2 of my Cybersecurity & Ethical Hacking practical program, I completed five modules covering multiple Kali Linux tools, GHDB footprinting, Maltego footprinting, theHarvester information gathering and Nmap network scanning.

These exercises helped me understand different approaches to reconnaissance and footprinting, how information from different tools can be reviewed, how relationships can be explored visually, and how Nmap can be used for host discovery in a lab environment.

I also learned the importance of validating tool output, documenting observations accurately, protecting sensitive information and staying within an authorized testing scope.

The five modules provided practical exposure to information gathering and network discovery, which are important activities in a broader penetration-testing workflow.

8. Evidence & Project Files

The project material is organized into the following folders:
Module	Project folder / report
PM1 – Multiple Kali Tools	PM1-Multiple-Kali-Tools/
PM2 – GHDB Footprinting	PM2-GHDB-Footprinting/
PM3 – Maltego Footprinting	PM3-Maltego-Footprinting/
PM4 – theHarvester Footprinting	PM4-theHarvester/reports/README.md
PM5 – Network Scanning	PM5-Network-Scanning/reports/README.md


Repository Structure
.
├── PM1-Multiple-Kali-Tools/
├── PM2-GHDB-Footprinting/
├── PM3-Maltego-Footprinting/
├── PM4-theHarvester/
│   └── reports/
│       └── README.md
├── PM5-Network-Scanning/
│   └── reports/
│       └── README.md
└── README.md

Evidence note: The PM4 and PM5 folders currently contain sanitized public summaries. This README does not link to sample screenshots from another person's repository or claim that unverified evidence is present. Add screenshots or detailed evidence links only after confirming that the files are yours, are in this repository, and are safe to publish.
End of Report

W2-PM-FINAL | Cybersecurity | Networkwalks | PM1–PM5
