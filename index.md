---
layout: default
---
<div>
    <a href="https://www.linkedin.com/in/simardeep1098"><img src="https://img.shields.io/badge/-LinkedIn-0072b1?&style=for-the-badge&logo=linkedin&logoColor=white" /></a>
    <a href="https://github.com/Simardeep1098"><img src="https://img.shields.io/badge/-GitHub-000000?&style=for-the-badge&logo=github&logoColor=white" /></a>
</div>

## Objective

This **SOC Deployment** project involved setting up a Security Operations Center (SOC) using Microsoft Sentinel to monitor and analyze security events in real-time. To simulate a real-world attack environment, the RDP port was deliberately left open to attract potential attackers, enabling the detection of malicious activity. A custom threat intelligence feed was integrated, providing real-time updates on new threats, while the Mitre ATT&CK framework focused on identifying Initial Access tactics to enhance early-stage threat detection.

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

### Resource Group Overview*

![](https://github.com/Simardeep1098/soc-deployment.github.io/blob/main/SOC%20Deployment/Screenshot%201.png?raw=true)

The Resource Group Overview page provides a comprehensive view of all associated resources, including the virtual machine, network security group, virtual network, and associated disks, illustrating the infrastructure setup for the SOC deployment.

### Sentinel Rule Query - General Success Activity

![](https://github.com/Simardeep1098/soc-deployment.github.io/blob/main/SOC%20Deployment/Screenshot%202.png?raw=true)

This screenshot displays the query that filters for general successful activities where Activity contains "success". Severity: Informational. This rule captures all successful login events, providing a baseline for monitoring and establishing normal activity patterns.

### Sentinel Rule Query - Success Activity Excluding System Accounts

![](https://github.com/Simardeep1098/soc-deployment.github.io/blob/main/SOC%20Deployment/Screenshot%203.png?raw=true)

The second screenshot shows the query that filters for successful activities while excluding system accounts: SecurityEvent | where Activity contains "success" and Account !contains "system". Severity: Medium. This rule refines the monitoring to focus on user accounts only, reducing noise from system accounts and highlighting potentially significant login events.

### Sentinel Rule Query - User Accounts Excluding Specific VM

![](https://github.com/Simardeep1098/soc-deployment.github.io/blob/main/SOC%20Deployment/Screenshot%204.png?raw=true)

The third screenshot illustrates the query that filters for user account activities excluding a specific VM: SecurityEvent | where AccountType contains "user" and Account !contains "SOCVM". Severity: High. This rule is set to high severity as it targets user activities while explicitly excluding a known device used for testing, increasing the likelihood of detecting unusual or unauthorized user behavior.

### Sentinel Overview

![](https://github.com/Simardeep1098/soc-deployment.github.io/blob/main/SOC%20Deployment/Screenshot%205.png?raw=true)

The Sentinel Overview page, captured an hour after deployment, showcases the collected events, generated alerts, and logs, demonstrating the effectiveness of the SOC setup in monitoring and detecting security activities.

## Conclusion

This project provided hands-on experience in SOC deployment, SIEM configuration, and enhanced detection using threat intelligence feeds, making it a valuable exercise for cybersecurity skill development.
