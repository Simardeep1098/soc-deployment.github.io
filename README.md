---
layout: default
title: SOC Deployment
---

# SOC Deployment

## Objective

This **SOC Deployment** project is aimed to create a fully functional Security Operations Center (SOC) using Microsoft Sentinel to monitor, analyze, and generate alerts for device activities. A threat intelligence feed was integrated to enhance the SIEM by bringing in commonly seen and newly found indicators of compromise (IOCs). The project was designed to improve understanding of log management, security event correlation, and threat detection strategies.

### Skills Learned
- SIEM deployment, configuration, and management.
- Threat intelligence integration to enhance detection capabilities.
- Log analysis and event correlation for effective monitoring.
- Security event monitoring and incident detection.
- Application of MITRE ATT&CK framework (Initial Access tactics).

### Tools Used
- **Azure Virtual Machine (VM)**: Hosted the environment for monitoring and SIEM deployment.
- **Microsoft Sentinel**: Deployed SIEM for log analysis and security monitoring.
- **Log Analytics Workspace**: Centralized log management for security event analysis.
- **Windows Security Events (via Azure Monitor Agent)**: Collected and analyzed security event logs.

## Steps

*Ref 1: Initial SOC Setup*

![SOC Setup Screenshot](https://imgur.com/screenshot1)

The above diagram represents the initial setup of the SOC environment using an Azure VM and Microsoft Sentinel. It includes configuring data connectors and setting up log analytics.

*Ref 2: Threat Intelligence Integration*

![Threat Intelligence Screenshot](https://imgur.com/screenshot2)

This screenshot shows the integration of a threat intelligence feed into the SIEM, enriching the environment with new IOCs for better detection capabilities.

*Ref 3: Log Analytics Workspace*

![Log Analytics Screenshot](https://imgur.com/screenshot3)

The above screenshot depicts the Log Analytics Workspace where Windows security events were ingested for analysis and event correlation.

## Conclusion

This project provided hands-on experience in SOC deployment, SIEM configuration, and enhanced detection using threat intelligence feeds, making it a valuable exercise for cybersecurity skill development.