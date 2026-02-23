# Incident Analysis: Malware Analysis and IoC Identification
**Date:** 01/12/2025
**Case Status:** Completed
**Severity:** High

## Executive Summary
This investigation centered on a suspicious spreadsheet detected at a financial services firm, which after executed by an employee, it began performing unauthorized actions, including the creation of multiple executable files. I was tasked with confirming the malicious nature of the file and extracting *Indicators of Compromise* to support incident response efforts.

## Technical Analysis (The 5 W's)
* **Who**: Detection triggered by an Intrusion Detection System (IDS) alert involving an employee download.
* **What:** Technical analysis of a suspicious spreadsheet via SHA256 hashing and threat intelligence.
* **When:** Investigation initiated at 1:20 p.m. following the alert generation.
* **Where:** Analysis focused on an employee endpoint within the corporate network.
* **Why:** Necessary to determine the threat level and identify behavioral patterns to prevent lateral movement.

## Technical Walkthrough
### Threat Assessment
The investigation involved a SHA256 hash of the suspicious file. I reviewed the corresponding *VirusTotal* report, where multiple security vendors had flagged the hash as malicious. The community score and vendor analysis confirmed that the file was a high-risk threat.

### Applying the Pyramid of Pain
To build a better defense, the threat was categorized using the *Pyramid of Pain* framework:
* **Hash Values & Network Indicators:** I identified secondary hashes and malicious IP addresses within the report for immediate blocking.
* **Behavioral Analysis:** I examined the sandbox results to understand the attacker's techniques, specifically the methods used to spawn new executable files on the system.

## Lessons Learned
This scenario emphasized that while blocking file hashes is a necessary first step, it is a low-level defense. I learned that true security resilience comes from identifying behavioral patterns (the top of the Pyramid of Pain). Because these techniques are difficult for threat actors to change, focusing detection efforts here provides a much higher level of long-term protection.
