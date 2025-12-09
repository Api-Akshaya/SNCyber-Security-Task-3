OWASP ZAP Vulnerability Assessment – Task 3
Overview

This project documents the vulnerability assessment performed on a practice web application hosted on Metasploitable2, using OWASP ZAP (Zed Attack Proxy).
The objective is to identify common web application vulnerabilities, understand their risks, and demonstrate the use of automated scanning tools in cybersecurity assessments.

Tools and Environment

Kali Linux (Attacker Machine)

OWASP ZAP (Web Application Security Scanner)

Metasploitable2 (Vulnerable Web Application)

Network Setup:

Kali Linux: NAT + Host-Only

Metasploitable2: Host-Only

Target URL:

http://192.168.56.101

Assessment Methodology

Launch the Metasploitable2 virtual machine and verify the target URL is accessible.

Open OWASP ZAP on Kali Linux.

Navigate to Automated Scan or Quick Start.

Enter the target URL and begin scanning.

Allow ZAP to crawl and analyze all reachable pages.

Review findings in the Alerts panel.

Document each vulnerability and explain its associated risk.

Key Vulnerabilities Identified

The OWASP ZAP scan generated multiple alerts across various severity levels.
Some of the notable findings include:

Medium Severity

Hash Disclosure – MD5 Crypt

Absence of Anti-CSRF Tokens

Application Error Disclosure

Vulnerable JavaScript Library

Information Disclosure – Debug Error Messages

Sensitive Information in URL

Low Severity

Directory Browsing

Missing Anti-clickjacking Header

Cookie Without HttpOnly Flag

Cookie Without SameSite Attribute

X-Content-Type-Options Header Missing

Informational Alerts

Server Leaks Information via Headers

Private IP Disclosure

Timestamp Disclosure

Suspicious Comments

Server Technology Exposure

Risk Explanation (Summary)
Hash Disclosure – MD5 Crypt

Weak or exposed hashes can be cracked offline, compromising credentials.

Absence of Anti-CSRF Tokens

Allows attackers to perform unauthorized actions on behalf of authenticated users.

Application Error Disclosure

Reveals internal server errors and paths that assist attackers in exploitation.

Content Security Policy Header Missing

Increases susceptibility to cross-site scripting attacks.

Directory Browsing Enabled

Exposes internal files and directory structures.

Missing Anti-clickjacking Header

Allows clickjacking through iframe-based attacks.

Weak Cookie Settings

Cookies lacking HttpOnly or SameSite flags can lead to session hijacking or CSRF attacks.

Information Disclosure Issues

Internal comments, private IPs, stack traces, timestamps, and server headers provide insights that attackers can use to craft targeted attacks.

Conclusion

The assessment confirmed that the Metasploitable2 environment contains numerous vulnerabilities caused by outdated software, insecure default configurations, and missing security controls.

Using OWASP ZAP provided a practical understanding of:

Automated scanning workflows

Identifying critical and non-critical vulnerabilities

The importance of secure coding and server configuration practices

This task demonstrates fundamental skills in vulnerability assessment and web application security analysis.
