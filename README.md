🚀 Windows Endpoint Monitoring Project (Wazuh SIEM)

This project demonstrates a complete Windows endpoint monitoring pipeline using Wazuh SIEM, Sysmon, Filebeat, and the Wazuh Windows Agent.
The goal is to collect security events from a Windows 10 machine, forward them to a Wazuh server (running on Ubuntu), and visualize the alerts using the Wazuh Dashboard.

The architecture diagram also includes future SOC automation components like Shuffle SOAR and TheHive, but those parts are not implemented in this project.
------------------------------------------------------------------------------------------------
🧑‍💻 Basics

Sysmon → Watches Windows activities (process creation, network, registry changes).

Filebeat → Sends Sysmon logs to the Wazuh server.

Wazuh Agent → Helps send Windows logs securely to the server.

Wazuh Server → Analyzes logs, detects threats, and shows alerts.

Wazuh Dashboard → The web interface where you view everything.

This project teaches you how security logs flow, how SIEM tools work, and how SOC analysts monitor endpoints.

------------------------------------------------------------------------------------------------
📌 Project Overview

Environment Used
________________________________________________________________________________________________
Component                             	Role
________________________________________________________________________________________________
1.Ubuntu VM	                            Wazuh Server (Manager, Indexer, Dashboard)
________________________________________________________________________________________________
2.Windows 10 VM                    	    Wazuh Agent + Sysmon + Filebeat
________________________________________________________________________________________________
3.Windows 11 Host                      	Access Wazuh Dashboard
________________________________________________________________________________________________

Goal

✔ Collect endpoint logs
✔ Forward to Wazuh Manager
✔ Parse, analyze, and visualize alerts
✔ Prepare for future SOC automation

------------------------------------------------------------------------------------------------
📌 Architecture Diagram

👉 SOC Automation Architecture Diagram

*Note:
This diagram was made using Draw.io.
It shows a complete SOC pipeline including TheHive and Shuffle SOAR, but only the Wazuh monitoring part is implemented in this project.

------------------------------------------------------------------------------------------------
📌 Prerequisites

VirtualBox or VMware

Ubuntu + Windows 10 + Windows 11

Basic networking (Host-only or NAT network)

Internet access for installation

Tools Installed

Wazuh Manager

Wazuh Indexer

Wazuh Dashboard

Wazuh Windows Agent

Sysmon

Filebeat

------------------------------------------------------------------------------------------------
📘 Installation Guides (PDFs)


________________________________________________________________________________________________
Component                                      	PDF Link
________________________________________________________________________________________________
Sysmon Setup + Wazuh Integration            	👉 Sysmon_Installation_and_Wazuh_Integration.pdf
________________________________________________________________________________________________
Wazuh Server Installation (Ubuntu 4.7.5)     	👉 Wazuh_Server_Installation_Ubuntu_4.7.5.pdf
________________________________________________________________________________________________
Wazuh Windows Agent Installation     	👉Wazuh_Windows_Agent_Installation_and_Registration.pdf
________________________________________________________________________________________________

------------------------------------------------------------------------------------------------

⚙️ Configuration Files
________________________________________________________________________________________________
Purpose                                   	File
________________________________________________________________________________________________
Sysmon Rules	                            👉 sysmonconfig.xml
________________________________________________________________________________________________
Wazuh Agent Config	                      👉 ossec.conf
________________________________________________________________________________________________
Filebeat Config	                          👉 filebeat.yml
________________________________________________________________________________________________

------------------------------------------------------------------------------------------------
📸 Screenshots

________________________________________________________________________________________________
Screenshot                          	 Link
________________________________________________________________________________________________
Windows 10 System Info	              win10-system-info.png
________________________________________________________________________________________________
Wazuh Manager Status                	wazuh-manager-status.png
________________________________________________________________________________________________
Wazuh Indexer Status	                wazuh-indexer-status.png
________________________________________________________________________________________________
Sysmon Running	                      sysmon_service_running.png
________________________________________________________________________________________________
Sysmon Events	                        Sysmon_Events_in_Event_View.png
________________________________________________________________________________________________
Dashboard Overview	                  wazuh-dashboard-overview.png
________________________________________________________________________________________________
Wazuh Agent List	                    Dashboard_wazuh_agent_list.png
________________________________________________________________________________________________
Filebeat Status                     	filebeat_status.png
________________________________________________________________________________________________
Dashboard Login                     	wazuh-dashboard-login.png
________________________________________________________________________________________________
Windows Agent Status	                win10-wazuh-agent-status.png
________________________________________________________________________________________________
Wazuh API Configuration	             Wazuh_API_configuration_page.png
________________________________________________________________________________________________
Ubuntu Version	                     ubuntu-version.png
________________________________________________________________________________________________

------------------------------------------------------------------------------------------------
🛠️ Steps Followed in This Project

Created Ubuntu and Windows 10 VMs

Installed Wazuh Server (Manager, Indexer, Dashboard)

Installed Wazuh Agent on Windows 10

Installed Sysmon with custom config

Installed Filebeat and enabled Sysmon module

Verified logs arriving in Wazuh Dashboard

Captured screenshots and generated documentation

------------------------------------------------------------------------------------------------

📁 Project Structure
/Architecture
/Screenshots
/Config-Files
/Installation-Guides
README.md
LICENSE

------------------------------------------------------------------------------------------------
📌 Project Status
✔ Fully Implemented

Wazuh Server

Windows Agent

Sysmon Monitoring

Filebeat Forwarding

Dashboard Visualization

------------------------------------------------------------------------------------------------
🔜 Future Enhancements

Shuffle SOAR automation

TheHive case management

Automated incident response

------------------------------------------------------------------------------------------------
🏁 Conclusion

This project provides a complete demonstration of Windows endpoint monitoring using Wazuh SIEM + Sysmon + Filebeat.
It helps beginners understand log collection, SIEM pipelines, and real-world SOC workflows.
The architecture also sets the foundation for future SOC automation and IR workflows.
------------------------------------------------------------------------------------------------
