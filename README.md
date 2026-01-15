# Windows Endpoint Monitoring Project (Wazuh SIEM)

This project demonstrates a complete Windows endpoint monitoring setup using Wazuh SIEM, Sysmon, Filebeat, and Wazuh Windows Agent.
Logs are collected from a Windows 10 endpoint, forwarded to a Wazuh server running on Ubuntu, and visualized in the Wazuh Dashboard.

The architecture diagram also includes future SOC automation using Shuffle SOAR and TheHive, but those parts are not implemented yet. They are shown only for learning and future expansion.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔹 Project Overview

Environment Used:

# Component	                                Role
 Ubuntu VM :                               	Wazuh Server (Manager, Indexer, Dashboard),
 Windows 10 VM :                           	Wazuh Agent + Sysmon + Filebeat,
 Windows 11 Host :                        	Access Wazuh Dashboard via browser.

 
Project Goal

✔ Collect Windows logs
✔ Forward them to Wazuh Manager
✔ Parse & analyze logs
✔ Display alerts in Wazuh Dashboard
✔ Prepare for future SOAR automation

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔹 Architecture Diagram

The architecture diagram was created using draw.io. It shows the full SOC automation pipeline (Wazuh → Shuffle → TheHive).
⚠ Only Wazuh + Sysmon + Filebeat parts are implemented in this project.
Shuffle & TheHive are included for future expansion.

👉 View Diagram:
SOC Automation Flow Diagram
File: SOC Automation flow diagram.drawio.png
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Architecture/SOC%20Automation%20flow%20diagram.drawio%20(1).png

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔹 Prerequisites

VirtualBox or VMware

Windows 10 VM

Ubuntu VM (20.04 or 22.04)

Basic VM networking (NAT / Host-only)

Internet access for installation

Tools Installed

Wazuh Manager

Wazuh Indexer

Wazuh Dashboard

Wazuh Windows Agent

Sysmon + Sysmon configuration

Filebeat

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔹 Installation Guides (PDFs)

👉 Sysmon Installation & Wazuh Integration
File: Sysmon_Installation_and_Wazuh_Integration.pdf
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Installation-Guides/Sysmon_Installation_and_Wazuh_Integration.pdf

👉 Wazuh Server Installation (Ubuntu 4.7.5)
File: Wazuh_Server_Installation_Ubuntu_4.7.5.pdf
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Installation-Guides/Wazuh_Server_Installation_Ubuntu_4.7.5.pdf

👉 Wazuh Windows Agent Installation
File: Wazuh_Windows_Agent_Installation_and_Registration.pdf
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Installation-Guides/Wazuh_Windows_Agent_Installation_and_Registration.pdf

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔹 Configuration Files

👉 Sysmon Configuration
File: sysmonconfig.xml
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Config-Files/sysmonconfig.xml

👉 Wazuh Agent Configuration
File: ossec.conf
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Config-Files/ossec.conf

👉 Filebeat Configuration
File: filebeat.yml
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Config-Files/filebeat.yml

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔹 Screenshots

All screenshots are stored in the /Screenshots folder.

✔ Windows 10 System Info

File: win10-system-info.png
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Screenshots/win10-system-info.png

✔ Wazuh Manager Status

File: wazuh-manager-status.png
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Screenshots/wazuh-manager-status.png

✔ Wazuh Indexer Status

File: wazuh-indexer-status.png
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Screenshots/wazuh-indexer-status.png

✔ Sysmon Service Running

File: sysmon_service_running.png
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Screenshots/sysmon_service_running.png

✔ Sysmon Events in Event Viewer

File: Sysmon_Events_in_Event_View.PNG
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Screenshots/Sysmon_Events_in_Event_View.PNG

✔ Wazuh Dashboard Overview

File: wazuh-dashboard-overview.png
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Screenshots/wazuh-dashboard-overview.png

✔ Wazuh Dashboard Login

File: wazuh-dashboard-login.png
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Screenshots/wazuh-dashboard-login.png

✔ Wazuh Agent List

File: Dashboard_wazuh_agent_list.png
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Screenshots/Dashboard_wazuh_agent_list.png

✔ Filebeat Status

File: filebeat_status.png
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Screenshots/filebeat_status.png

✔ Windows Agent Status

File: win10-wazuh-agent-status.png
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Screenshots/win10-wazuh-agent-status.png

✔ Ubuntu Version

File: ubuntu-version.png
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Screenshots/ubuntu-version.png

✔ Wazuh API Configuration Page

File: Wazuh_API_configuration_page.png
https://github.com/dnyaneshpadol/Windows-Endpoint-Monitoring-Project-Wazuh-SIEM-/blob/main/Screenshots/Wazuh_API_configuration_page.png

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔹 Steps Followed in This Project

Created Ubuntu & Windows 10 VMs

Installed Wazuh Server (Manager, Indexer, Dashboard)

Installed Wazuh Windows Agent

Installed Sysmon with configuration

Installed Filebeat and enabled Sysmon module

Verified logs in the Wazuh Dashboard

Captured and documented results

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔹 Project Structure
/Architecture

/Screenshots

/Config-Files

/Installation-Guides

README.md

LICENSE

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔹 Project Status
✔ Fully Implemented

Wazuh Server

Wazuh Windows Agent

Sysmon Logging

Filebeat Forwarding

Dashboard Monitoring

🔜 Future Enhancements

Shuffle SOAR automation

TheHive case management

Automated response workflows

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔹 Conclusion

This project demonstrates an end-to-end implementation of Windows endpoint monitoring using Wazuh + Sysmon + Filebeat.
It provides a strong foundation for real SOC operations and future automation.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
