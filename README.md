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
