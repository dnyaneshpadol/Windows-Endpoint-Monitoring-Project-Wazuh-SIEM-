Windows Endpoint Monitoring Project using Wazuh SIEM

This project demonstrates a simple endpoint monitoring setup using Wazuh SIEM, Sysmon, Filebeat, and the Wazuh Windows Agent.
Security events from a Windows 10 machine are collected and visualized in the Wazuh Dashboard hosted on an Ubuntu server.
------------------------------------------------------------------------------------------------
📌 Project Overview

Environment used:

Ubuntu VM → Wazuh Server (Manager, Indexer, Dashboard)

Windows 10 VM → Wazuh Agent + Sysmon + Filebeat

Windows 11 Host → Access Wazuh Dashboard through browser

Goal:
Collect Windows event logs (via Sysmon), forward them to the Wazuh server, and monitor everything in real time.

A future plan (shown in the architecture diagram) includes automation using Shuffle SOAR and TheHive.
------------------------------------------------------------------------------------------------
📌 Architecture Overview

The architecture is simple:

Windows 10 endpoint generates events (Sysmon, Event Logs).

Wazuh Agent forwards events to the Wazuh Manager.

Wazuh Manager + Indexer processes and stores logs.

Wazuh Dashboard visualizes alerts.

Windows 11 host accesses the dashboard over HTTPS.

The diagram also includes future workflow components (Shuffle SOAR and TheHive) for alert enrichment and automation.
------------------------------------------------------------------------------------------------
📌 Prerequisites

VirtualBox (or VMware)

Ability to run 2 VMs + host

Basic network connectivity between VMs

VMs Used

Ubuntu 20.04/22.04 → Wazuh Server

Windows 10 → Agent, Sysmon, Filebeat

Windows 11 → Dashboard access

Tools Installed

Wazuh Manager, Indexer, Dashboard

Wazuh Windows Agent

Sysmon + Sysmon config (SwiftOnSecurity)

Filebeat for Sysmon log forwarding
------------------------------------------------------------------------------------------------
📌 Installation Overview
1. Wazuh Server (Ubuntu VM)

Download Wazuh installation script

Install Indexer, Manager, Dashboard

Access dashboard via:

https://<ubuntu-ip>

2. Windows 10 Agent

Download Windows agent from Wazuh dashboard

Enter Manager IP + enrollment key

Start Wazuh service from services.msc

3. Sysmon

Install Sysmon:

sysmon64.exe -accepteula -i sysmonconfig.xml

4. Filebeat

Install Filebeat

Enable Sysmon module

Start Filebeat service
------------------------------------------------------------------------------------------------
📌 Steps Followed in This Project

Created Ubuntu and Windows 10 VMs

Installed Wazuh Server on Ubuntu

Installed Wazuh Agent on Windows 10

Installed Sysmon + config

Installed Filebeat to forward Sysmon logs

Verified:

Agent connected

Sysmon events received

Alerts visible in dashboard

Captured screenshots and documented results

📸 Screenshots Included

Wazuh dashboard login

Dashboard overview

Wazuh agent list

Filebeat status

Sysmon service running

Sysmon events in Event Viewer

Ubuntu version & Wazuh services

Manager & Indexer status logs

Windows 10 system information

Wazuh agent status on Windows

All screenshots are stored in the /Screenshots folder.
------------------------------------------------------------------------------------------------
📁 Project Structure
/Architecture
/Screenshots
/Installation-Guides
/Config-Files
README.md
LICENSE
------------------------------------------------------------------------------------------------
📌 Status of the Project
✔ Fully Implemented

Wazuh Server

Wazuh Agent

Sysmon

Filebeat

Dashboard Monitoring

🔜 Planned (Future Work)

Shuffle SOAR automation

TheHive case management

Automatic response workflows
------------------------------------------------------------------------------------------------
📌 Conclusion

This project provides a working setup of endpoint monitoring using Wazuh SIEM and Sysmon.
It shows how logs move from a Windows endpoint to a centralized server and how alerts are visualized in the Wazuh Dashboard.
------------------------------------------------------------------------------------------------

