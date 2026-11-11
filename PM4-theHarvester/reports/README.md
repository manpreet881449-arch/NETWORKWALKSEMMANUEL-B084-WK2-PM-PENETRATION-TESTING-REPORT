# PM4 – theHarvester Footprinting

## 1. Project Overview

**Project Name:** PM4 – theHarvester Footprinting  
**Module:** Week 2 – Cybersecurity Project  
**Category:** OSINT (Open-Source Intelligence)  
**Tool:** theHarvester  
**Tool Version:** 4.11.1  
**Operating System:** Kali Linux

## 2. Objective

The objective of this practical exercise is to perform passive information gathering using theHarvester, an OSINT tool used during the reconnaissance and footprinting phase of a penetration testing engagement.

The exercise focuses on collecting publicly available information associated with target domains, including:

- Domain-related information.
- Publicly indexed hostnames and subdomains.
- Email addresses, when available.
- Publicly available employee or people-related information, when supported by the selected source.
- Information from supported search engines and OSINT providers.

The purpose is to understand how publicly available information can help security professionals identify an organization's external digital footprint.

## 3. Tools and Environment

| Component | Details |
|---|---|
| Operating System | Kali Linux |
| Tool | theHarvester |
| Version | 4.11.1 |
| Technique | Passive Information Gathering |
| Search Provider | Baidu |
| Additional Provider Test | All supported sources (requested) |
| Target Domains | microsoft.com and google.com |

## 4. About theHarvester

theHarvester is an open-source intelligence (OSINT) tool developed by Christian Martorella from Edge-Security Research.

It is commonly used during the reconnaissance phase of penetration testing to collect publicly available information about an organization or domain.

It supports multiple information sources, including search engines, certificate transparency services, threat intelligence platforms, and other public information providers.

The information gathered can help security professionals understand an organization's publicly visible infrastructure.

## 5. Command-Line Help and Options

### Command 1: Display Help

```bash
theHarvester -h
```

**Purpose:**

Displays the help menu, including available command-line arguments, supported data sources, and usage instructions.

Important options:

| Option | Description |
|---|---|
| `-h` | Display help information. |
| `-d` | Specify the target domain. |
| `-l` | Set the maximum number of search results. |
| `-S` | Specify the starting result number. |
| `-b` | Select the data source. |
| `-f` | Save results in XML and JSON formats. |
| `-p` | Use configured proxies. |
| `-s` | Query Shodan for discovered hosts. |
| `-r` | Perform DNS resolution on discovered subdomains. |
| `-n` | Enable DNS lookup. |
| `-c` | Perform DNS brute-force enumeration. |
| `-t` | Check for potential subdomain takeovers. |
| `-q` | Suppress missing API key warnings. |

**Observed Output:**

- theHarvester version: 4.11.1
- Configuration file: `/etc/theHarvester/proxies.yaml`
- Help menu successfully displayed.
- Multiple supported OSINT data sources were listed.

## 6. Practical Execution

### Task 1: Passive Footprinting of Microsoft

**Command:**

```bash
theHarvester -d microsoft.com -l 1000 -b baidu 2>&1 | tee outputs/task1-baidu.txt
```

**Command Breakdown:**

- `theHarvester`: Executes the OSINT tool.
- `-d microsoft.com`: Specifies Microsoft as the target domain.
- `-l 1000`: Sets the maximum result limit to 1000.
- `-b baidu`: Selects Baidu as the information source.
- `2>&1`: Redirects standard error into standard output.
- `tee`: Displays the command output in the terminal and saves it to a file.
- `outputs/task1-baidu.txt`: Stores the execution log.

**Observed Results:**

Target: `microsoft.com`

Data source: Baidu

The tool reported:

- IP addresses found: 0
- Email addresses found: 0
- People found: 0
- Hostnames found: 6

**Discovered Hostnames:**

1. account.microsoft.com
2. admin.exchange.microsoft.com
3. developer.microsoft.com
4. spf-c.microsoft.com
5. support.microsoft.com
6. ti.defender.microsoft.com

**Analysis:**

The Baidu source returned six hostnames associated with the Microsoft domain.

These results demonstrate how passive OSINT techniques can identify publicly indexed subdomains and hostnames without directly scanning the target infrastructure.

No IP addresses, email addresses, or people-related records were returned by this particular search.

The discovered hostnames represent publicly indexed information and should not automatically be considered vulnerabilities.

## 7. Additional Commands Used

### Task 2: Google Domain Footprinting Using Baidu

```bash
theHarvester -d google.com -l 1000 -b baidu 2>&1 | tee outputs/task2-baidu.txt
```

**Purpose:**

To perform a second passive information-gathering exercise against the Google domain using Baidu as the selected source.

The result file is saved separately to preserve the Microsoft and Google execution logs.

**Expected Analysis:**

The execution output should be reviewed for:

- Discovered hostnames.
- Publicly indexed email addresses.
- People-related information.
- IP address information.

Note: The Google execution output was not included in the supplied results, so no findings are claimed for this task.

### Task 3: Google Footprinting Using All Sources

```bash
theHarvester -d google.com -l 50 -b all 2>&1 | tee outputs/task3-all-sources.txt
```

**Purpose:**

To attempt information gathering against Google using the `all` source selection and a result limit of 50.

This command was included in the practical testing process to explore multiple information sources.

**Important Technical Note:**

The supplied theHarvester 4.11.1 help output lists individual supported providers, but does not explicitly document `all` as a valid source.

Therefore, this command should be treated as an attempted test until its actual terminal output confirms whether it was accepted and which providers were queried.

No results are claimed without the corresponding execution output.

## 8. Results and Observations

| Test | Target | Source | Result |
|---|---|---|---|
| Help menu | N/A | N/A | Successfully displayed |
| Task 1 | microsoft.com | Baidu | 6 hostnames |
| Task 2 | google.com | Baidu | Output pending |
| Task 3 | google.com | All | Execution result pending |

### Key Observations

1. TheHarvester successfully executed on Kali Linux.
2. The help menu displayed version 4.11.1 and supported data sources.
3. The Microsoft Baidu search returned six publicly indexed hostnames.
4. No IP addresses, email addresses, or people-related records were returned in the Microsoft test.
5. Different OSINT providers may return different results depending on their indexing, availability, and access requirements.
6. Some providers may return API-key warnings, response-format warnings, or incomplete results.

## 9. Limitations

During OSINT information gathering, several limitations may affect the results:

- Search engines may not index every publicly accessible hostname.
- Some providers require API keys.
- Search provider access and response formats may change.
- Rate limits may restrict the number of requests.
- Some sources may return incomplete or no results.
- A hostname discovery does not establish that the hostname is vulnerable.
- Results should be independently validated before being used in a security assessment.

## 10. Security and Ethical Considerations

This exercise focuses on passive information gathering using publicly available information.

Security testing must always be performed within an authorized scope.

The following precautions were considered:

- Only publicly available information was considered.
- No unauthorized exploitation was performed.
- No authentication bypass or intrusive testing was conducted.
- Discovered hostnames are documented as reconnaissance findings, not confirmed vulnerabilities.
- Potentially sensitive information and raw output files are excluded from the public repository.

## 11. Data Protection

Raw output files and potentially sensitive information are not included in this public repository.

Only selected, non-sensitive findings and project documentation are intended for publication.

This helps prevent accidental disclosure of sensitive reconnaissance data.

## 12. Conclusion

This practical exercise demonstrated the use of theHarvester 4.11.1 for passive OSINT-based footprinting.

The Microsoft domain test using Baidu successfully identified six publicly indexed hostnames.

The exercise provided practical experience with command-line execution, selecting OSINT information sources, collecting hostname information, saving terminal output, and interpreting reconnaissance findings.

It also demonstrated that OSINT results depend on the availability and reliability of external information sources.

Overall, the exercise strengthened understanding of passive reconnaissance and its role in the initial stages of a penetration testing engagement.

## 13. Repository Structure

```text
PM4-theHarvester/
│
├── README.md
│
├── outputs/
│   ├── task1-baidu.txt
│   ├── task2-baidu.txt
│   └── task3-all-sources.txt
│
└── screenshots/
    ├── 01-theHarvester-help.png
    ├── 02-microsoft-baidu-results.png
    ├── 03-google-baidu-results.png
    └── 04-google-all-sources.png
```

Note: The outputs and screenshots folders may be maintained locally. Do not upload raw logs or screenshots containing sensitive information to a public repository.
