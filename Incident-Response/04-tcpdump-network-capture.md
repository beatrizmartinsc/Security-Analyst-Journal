# Incident Analysis: Network Traffic Analysis via Command Line (tcpdump)
**Date:** 01/12/2025
**Case Status:** Completed

## Executive Summary
I was tasked with capturing and analyzing live network traffic directly from a Linux terminal. Unlike using a graphical tool like Wireshark, this scenario required me to use **tcpdump* to monitor the 'eth0' interface. The goal was to generate specific traffic, capture it in real-time, and filter the results to find relevant security data. 

## Technical Analysis (The 5 W's)
* **Who**: I acted as the analyst responsible for monitoring interface traffic.
* **What:** I captured and filtered live packets, focusing on header details and communication patterns.
* **When:** I performed this analysis during a technical lab session.
* **Where:** I used a Linux Virtual Machine to interact to the Command-Line interface
* **Why:** I conducted this analysis to build foundational skills in network traffic inspection and to support the detection and analysis phase of incident response. 

## Technical Walkthrough
### How I Managed the Traffic
I started by identifying the available network interfaces using the **ifconfig* command and **tcpdump -D*. Once I identified 'eth0' as the active interface, I executed captures and filtered using **tcpdump* with interface, port, and packet count options, and used the **curl* command to generate HTTP traffic for analysis. 

### Key Skills I applied
* **Interface Identification:** I verified which network interfaces were available for monitoring.
* **Targeted Capturing:** I used specific **tcpdump* options to limit the data I collected, ensuring the logs remained manageable. 
* **Traffic Generation:** I used command-line tools to create  checked the actual data being sent to ensure the communication matched the "test" traffic so I could verify that my monitoring was working correctly.

## Lessons Learned
I realized that being comfortable with Linux terminal is essential for a Security Analyst. In many real-world situations, you may only have access to a command-line to investigate a compromised server. I learned that **tcpdump* is powerful, lightweight tool for quick investigations when needed.
