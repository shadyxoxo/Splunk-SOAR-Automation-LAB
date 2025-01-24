# Splunk SOAR Automation LAB

## Objective
The Splunk SOAR Automation Detection Lab project was designed to establish a controlled environment for simulating and detecting cyberattacks. Its primary objective is to ingest and analyze logs within a Security Information and Event Management (SIEM) system, creating realistic test telemetry to replicate real-world attack scenarios.

In this lab, two Splunk SOAR playbooks were developed:

Playbook 1: RDP Brute Force Attack Detection:
This playbook identifies potential Remote Desktop Protocol (RDP) brute force attacks by analyzing logs.
Unlike Playbook 1, it does not take responsive actions but focuses solely on detection and raising alerts for malicious activity.
This hands-on experience provided practical exposure to Splunk, SOAR automation, network security, attack patterns, and defensive strategies, enhancing the understanding of advanced cybersecurity concepts.

Playbook 2: Unfamiliar Successful Sign-In Detection:
This playbook detects unfamiliar successful login events generated in Splunk.
It performs IP reputation checks using AbuseIPDB and VirusTotal. Based on the reputation scores, the event is flagged as malicious or benign.
If flagged as malicious, the playbook interacts with Active Directory (AD) to prompt the user or analyst to disable the associated user account.

### Skills Learned
- Advanced SIEM Concepts:
  In-depth understanding of log ingestion, analysis, and operational workflows in a SIEM environment.
- Log Analysis and Correlation:
  Proficiency in analyzing and correlating network logs to detect anomalies and pinpoint security incidents.
- Attack Signature Recognition:
  Ability to create and recognize patterns associated with various attack types (e.g., brute force, phishing, privilege escalation).
- Network Security and Protocols:
  Enhanced knowledge of network protocols (TCP/IP, RDP, etc.), security vulnerabilities, and defensive strategies.
- Incident Response Automation:
  Hands-on experience in automating incident response processes using Splunk SOAR playbooks.
- Threat Intelligence Integration:
  Knowledge of integrating external threat intelligence platforms like AbuseIPDB and VirusTotal for reputation scoring.
- Active Directory Security:
  Practical experience in managing and securing Active Directory accounts and group policies in response to threats.
- Critical Thinking and Problem-Solving:
  Improved ability to assess and respond to dynamic cybersecurity scenarios.
- Telemetry Simulation: Expertise in generating realistic telemetry data to emulate real-world attacks.
   Playbook Design and Testing: Advanced skills in designing, implementing, and refining SOAR playbooks for specific use cases.

### Tools Used
- Security Information and Event Management (SIEM): Splunk for log ingestion, analysis, and alert correlation.
- Splunk SOAR: For designing automated playbooks to detect and respond to cybersecurity threats.
- Wireshark: For capturing and analyzing network traffic in detail.
- AbuseIPDB and VirusTotal: Integrated for IP reputation checks and malicious activity scoring.
- Active Directory (AD): Used for managing user accounts, group policies, and executing responsive actions like account disabling.
- Telemetry Generation Tools: Tools like Caldera, AttackIQ, or custom scripts to simulate attack scenarios and generate realistic logs.
- Threat Intelligence Platforms: Utilized external threat feeds to enhance detection capabilities.
- Scripting and Automation: Python and PowerShell for scripting playbook actions, log parsing, and custom detection scenarios.
- Virtualized Environments: VMware or VirtualBox for creating isolated lab setups to replicate attacks safely.
- Dashboards and Visualization: Splunk’s dashboards for real-time monitoring and analysis of security events.
- Endpoint Security Tools: microsoft endpoint security, used to monitor and correlate host-level events.

#Playbook 1 
- Inbound RDP Brute Force Attack.
- IP Reputation (Source) Abuse IPDB & Virus Total.
- If the score Of AbuseIPDB is >= 75% or Virus Total is >= 5 Vendor Flags it as malicious.
- Output will be “Big Bad Evil or Malicious” otherwise output “Further Investigation Required”.
<div>
  <img src="https://i.imgur.com/JPwHLng.png" alt="Playbook 1 Diagram" width="600">
</div>
*Ref 1: Network Diagram (Inbound RDP Brute Force Attack)*




#Playbook 2 Responsive Action from AD to Prompt Analyst or User to Disable Account.
- Unfamiliar Successful Sign Ins.
- IP Reputation (Source) Abuse IPDB & Virus Total.
- If the score Of AbuseIPDB is >= 85% or Virus Total is >= 5 Vendor Flags it as malicious.
- Automatically Disable User Account Otherwise Prompt User If they want to disable the account.
<div>
  <img src="https://imgur.com/HFs5fed.png" alt="Playbook 2 Diagram" width="600">
</div>
*Ref 2: Network Diagram (Unfamiliar Successful Sign Ins)*

