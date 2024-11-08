# Incident Response Report - ENPM685 Waffle Co

This repository contains documentation and findings from a security incident investigation conducted for ENPM685 Waffle Co. The report analyzes the breach, identifying the vulnerabilities exploited and providing recommendations to enhance security for the company's web and data infrastructure.

## Background

ENPM685 Waffle Co started as a small waffle shop and grew rapidly after launching a mobile app offering "push button, get waffle" service. The popularity of their proprietary "avocado waffle" expanded the customer base, bringing significant growth and attention to the business. However, a recent security breach exposed vulnerabilities in the company's development environment.

The breach investigation began after Nathan, the former cashier turned web developer, discovered an unauthorized Pastebin post claiming to have access to the company’s data. He suspected the breach might be related to the development website where he had used production data. This report details the findings and offers solutions to address the identified vulnerabilities.

## Objective

The goal of this investigation and report is to:

- Identify how the attacker gained unauthorized access to the system.
- Understand the actions performed by the attacker post-breach.
- Determine if sensitive data was accessed or exfiltrated.
- Provide actionable recommendations to mitigate future security risks.

## Methodology

The investigation follows a structured analysis approach:

1. **Data Collection**: Gather logs, server data, and network captures provided by Nathan.
2. **Log and Traffic Analysis**: Review system logs and network captures to trace the attacker’s activities.
3. **Attack Narrative**: Reconstruct the steps taken by the attacker from initial access to data exfiltration.
4. **Impact Assessment**: Assess whether sensitive data was accessed or stolen.
5. **Reporting**: Document findings, vulnerabilities, and provide recommendations.

## Key Findings

The following highlights some critical vulnerabilities discovered during the investigation:

- **Unsecured Development Environment**: Production data was used in a development environment accessible to external threats.
- **Weak Authentication Controls**: No multi-factor authentication or strong password policies, leading to easy account compromise.
- **File Upload Vulnerability**: An upload functionality allowed the attacker to upload malicious scripts, resulting in remote code execution.
- **Unauthorized SSH Access**: The attacker accessed sensitive data and modified user credentials through SSH.
- **Lack of Access Control**: Sensitive data was accessible without adequate restrictions.

## Recommendations

1. **Strengthen Authentication**: Enforce strong passwords, password expiration policies, and implement multi-factor authentication (MFA) for all sensitive access.
2. **Secure Development Environment**: Segregate development and production environments to prevent exposure of production data.
3. **Enhance File Upload Security**: Restrict file types, scan uploaded files for potential malware, and apply strict permissions.
4. **Implement Least Privilege Access**: Restrict access to sensitive data based on role and necessity.
5. **Regular Log Monitoring**: Implement regular log review and anomaly detection to catch unauthorized activities early.

## Conclusion

This investigation reveals that ENPM685 Waffle Co’s IT infrastructure lacks critical security measures, exposing it to potential threats. By addressing the recommendations above, the company can significantly reduce the risk of future breaches and improve its security posture.

For complete details, please refer to the full report in this repository.
