# Project 3: SIEM Deployment and Attack Simulation

## Project Overview
This project focused on deploying a Security Information and Event Management (SIEM) solution using Splunk Cloud to collect, centralise, and monitor security events from Linux and Windows endpoints.

The project also involved controlled attack simulations to examine how security events could be detected and investigated through centralised logging.

This was a collaborative project completed as part of the TechCrush Cybersecurity Capstone, Cohort 8.

## Objectives
- Deploy and configure Splunk Universal Forwarders on Linux and Windows endpoints.
- Forward endpoint logs to Splunk Cloud.
- Monitor and analyse security events.
- Conduct controlled attack simulations.
- Identify suspicious activities through relevant event logs.
- Document findings and recommend security improvements.

## Tools and Technologies
- Splunk Cloud
- Splunk Universal Forwarder
- Kali Linux
- Linux
- Windows
- Hydra
- Windows Event Logs
- Linux authentication and system logs
- MITRE ATT&CK Framework

## SIEM Deployment and Log Collection
Splunk Universal Forwarders were configured on Linux and Windows endpoints to send logs to Splunk Cloud.

The project report documented the following collected events:

- Linux: 1,190 events from `/var/log/auth.log` and `/var/log/syslog`.
- Windows: 114 events from System, Security, and Application event logs.

This centralised logging provided a basis for monitoring and investigating endpoint activities.

## Controlled Attack Simulations

### 1. Hidden Local Administrator Account Creation
A controlled Windows security test involved creating a hidden local administrator account named `hiddenadmin` and adding it to the local Administrators group.

Splunk detected relevant Windows security events:
- Event ID 4720 – User account created.
- Event ID 4732 – Member added to a security-enabled local group.

### 2. SSH Brute-Force Simulation
A controlled SSH brute-force simulation was conducted from Kali Linux using Hydra against the Linux endpoint.

The activity generated 126 failed password events, which were collected for monitoring and analysis.

### 3. Windows Security Log Clearing
A controlled test involved clearing the Windows Security event log using the `wevtutil` command.

Splunk detected Event ID 1102, which records the clearing of the Security audit log.

The project report also documented how off-host log forwarding preserved previously forwarded events after the local Security log was cleared.

## Incident Investigation
An incident report was prepared for the Windows Security log-clearing activity.

The activity was associated with the MITRE ATT&CK technique **T1070.001 – Clear Windows Event Logs**, under the Defense Evasion tactic.

The report documented the event, its security implications, and recommended monitoring and preventive measures.

## Key Findings and Learning Outcomes
- Understanding SIEM deployment and centralised log collection.
- Exposure to Linux and Windows security event monitoring.
- Understanding how account creation and privilege-group changes can be detected.
- Recognising failed SSH authentication attempts through endpoint logs.
- Understanding the security implications of event-log clearing.
- Using event identifiers to support security investigations.
- Applying MITRE ATT&CK to classify suspicious activity.
- Understanding the importance of off-host log forwarding.

## Recommendations
- Configure alerts for Windows Security Event ID 1102.
- Restrict permissions to clear Windows Security logs.
- Maintain continuous forwarding of endpoint logs to a centralised SIEM.
- Monitor suspicious account creation and administrator-group changes.
- Investigate repeated failed SSH authentication attempts.

## Participation
This was a collaborative TechCrush Cybersecurity Capstone project. I participated in the initial implementation and followed up with the other team members throughout the project until its completion. My hands-on participation was interrupted because my system ran out of storage.

The completed project findings documented here reflect the team's final work and are not presented as activities I personally completed in full.

## Disclaimer
All attack simulations were conducted in controlled educational lab environments. Sensitive tenant information, credentials, and personal details have been excluded from this documentation.