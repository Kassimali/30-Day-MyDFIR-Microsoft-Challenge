Week One: Microsoft Sentinel SOC Lab

MYDFIR Forge — 30-Day Microsoft Challenge

Project Overview

As part of the MYDFIR Forge 30-Day Microsoft Challenge, I completed Week One by building a hands-on Security Operations Center (SOC) lab using Microsoft Sentinel, a cloud-based SIEM solution.

The main goal was to build a working security monitoring environment, collect and analyze security logs, create detection rules, investigate alerts, and practice threat hunting using Kusto Query Language (KQL).

Task 1: Set Up the Microsoft Sentinel Lab

I created an Azure environment and deployed the following resources:

Windows Virtual Machine: Deployed a Windows VM to support security monitoring and lab activities.

Azure Resource Group: Created a resource group named mydifir-kassim-RG in the East US region to organize the lab resources.

Log Analytics Workspace: Created a workspace named mydifir-kassim-LAW to collect, store, and query security data.

Microsoft Sentinel: Added Sentinel to the Log Analytics workspace to enable security monitoring, detection, investigation, and threat hunting.

Microsoft Sentinel Training Lab: Deployed the training lab to populate the environment with sample security data for detection and investigation exercises.

Task 2: Create and Investigate a Brute-Force Detection

After setting up the environment, I moved on to practical SOC activities.

I created a Microsoft Sentinel analytics rule to detect repeated failed authentication attempts and configured it to run every five minutes.

I then investigated the generated alert and analyzed the available authentication events to understand the activity and determine whether the evidence supported a successful compromise.

This exercise helped me understand how analytics rules can identify suspicious authentication patterns and why alerts require further investigation before reaching a conclusion.

Task 3: Perform Threat Hunting Using KQL

I used Kusto Query Language (KQL) to search and analyze security data, identify suspicious activity, and investigate potential indicators of attack.

During the threat-hunting exercise, I:

Queried OfficeActivity_CL for suspicious activity.

Identified suspicious IP addresses for further investigation.

Used threat intelligence to support the investigation of potential indicators of compromise (IOCs).

Created Microsoft Sentinel bookmarks to preserve relevant findings for future reference.

Practiced writing KQL queries to identify and investigate potentially malicious activity.

I also explored Microsoft Defender Threat Intelligence (MDTI) to understand how threat intelligence can support threat hunting and investigation.

Task 4: Troubleshoot the Training Lab Deployment

Deploying the Microsoft Sentinel Training Lab presented several challenges.

The sample data was no longer available directly through Content Hub, so I used the deployment script provided in the Microsoft Sentinel GitHub repository.

The deployment initially failed because the script attempted to create another Azure Automation account, while my trial subscription was subject to a regional limit allowing only one Automation account.

I worked through the subscription upgrade process and contacted Microsoft Support when the upgrade encountered an issue. After Microsoft Support resolved the problem, I upgraded the subscription and successfully deployed the training lab.

This experience strengthened my Azure troubleshooting skills and taught me the importance of investigating deployment errors, understanding cloud resource limitations, and identifying root causes systematically.

## Screenshots

### Microsoft Sentinel Dashboard

![Microsoft Sentinel Dashboard](./screenshots/sentinel-dashboard.png)

### Brute-Force Analytics Rule

![Brute-Force Analytics Rule](./screenshots/brute-force-alert.png)

### Threat Hunting

![Threat Hunting](./screenshots/threat-hunting.png)

### Sentinel Training Lab



## Reflection 

This project helped me move from learning security concepts to applying them in a practical SOC environment.

I gained a better understanding of how security logs are collected and analyzed in Microsoft Sentinel, how KQL can be used to investigate security events, and how analytics rules can help identify suspicious activity.

The deployment challenges were also an important part of the learning experience. Troubleshooting the failed Training Lab deployment required me to investigate Azure resources, understand subscription limitations, resolve a subscription upgrade issue, and work with Microsoft Support.

One important lesson I learned is that a large number of security events does not automatically mean an attack was successful. Effective investigation requires context, correlation, and sufficient evidence before reaching a conclusion.

I will continue building on these skills in the following projects of the MYDFIR Forge 30-Day Microsoft Challenge.