# Detection Lab

## Objective
The Detection Lab project aimed to establish a controlled environment for simulating and detecting cyber attacks. The primary focus was to ingest and analyze logs within a Security Information and Event Management (SIEM) system, generating test telemetry to mimic real-world attack scenarios. This hands-on experience was designed to deepen understanding of network security, attack patterns, and defensive strategies.

### Skills Learned
- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used
- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

# Playbook 1
Inbound RDP Brute Force Attack.
•	IP Reputation (Source) <Abuse IPDB> & <Virus Total>.
•	If the score Of AbuseIPDB is >= 75% or Virus Total is >= 5 Vendor Flags it as malicious.
•	Output will be “Big Bad Evil or Malicious” otherwise output “Further Investigation Required”

# Playbook 2 Responsive Action from AD to Prompt Analyst or User to Disable Account.
Unfamiliar Successful Sign Ins.
•	IP Reputation (Source) <Abuse IPDB> & <Virus Total>.
•	If the score Of AbuseIPDB is >= 85% or Virus Total is >= 5 Vendor Flags it as malicious.
•	Automatically Disable User Account Otherwise Prompt User If they want to disable the account.



*Ref 1: Network Diagram*
