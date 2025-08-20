# Microsoft Azure Sentinel + ServiceNow Mini Lab

## Overview
This mini-project demonstrates how Microsoft Azure Sentinel can detect suspicious activity and integrate with ServiceNow for incident management. The goal is to simulate a basic SOC workflow using cloud SIEM detections and ITSM ticketing.

## Objectives
- Deploy Microsoft Azure Sentinel with a test log source
- Create two detection rules:
  1. Failed Login Attempts
  2. Suspicious IP Geolocation
- Simulate incident tracking in ServiceNow

## Setup
1. Create an Azure Free Account and enable **Microsoft Sentinel** on a Log Analytics Workspace.
2. Connect a test log source (e.g., Azure Activity Logs).
3. Create detection rules:
   - **Failed Logins**: Trigger after multiple failed sign-ins.
   - **Suspicious IP**: Trigger on sign-ins from unusual geolocations.

## ServiceNow Workflow
When alerts are triggered in Sentinel:
- A **mock ServiceNow ticket** is created with fields like:
  - Incident ID
  - Alert Type
  - Assigned To
  - Status
  - Resolution

Example Ticket:
Incident ID: INC-1001
Alert Type: Failed Login Attempts
Assigned To: SOC Analyst
Status: Resolved
Resolution: User account locked, password reset required.


## MITRE ATT&CK Mapping
- **Failed Logins** → T1110 (Brute Force)  
- **Suspicious IP Geolocation** → T1078 (Valid Accounts)

## Screenshots
*(Insert screenshots here)*  
- ![Sentinel Dashboard](images/sentinel-dashboard.png)  
- ![Detection Rule](images/failed-login-rule.png)  
- ![ServiceNow Ticket](images/servicenow-ticket.png)  

## Conclusion
This lab demonstrates how SOC teams can use Microsoft Azure Sentinel for cloud-based threat detection and ServiceNow for streamlined incident management.
