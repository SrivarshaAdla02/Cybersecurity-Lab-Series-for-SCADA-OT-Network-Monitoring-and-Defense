# 🔧 Cybersecurity Lab Series for SCADA & OT Network Monitoring and Defense

This repository provides documentation for a comprehensive virtual lab environment developed to support industrial network security testing and monitoring. The lab setup emulates a segmented network architecture and utilizes open-source tools such as Security Onion, pfSense, Snort, Wazuh, and Sysmon, with event visualization handled via Kibana.

---

## 📁 Repository Structure

| File Name                                           | Description                                                      |
|----------------------------------------------------|------------------------------------------------------------------|
| Lab0 - Virtual Box Network Setup.docx              | Configuration of NAT-based network segmentation in VirtualBox across internal, external, and DMZ zones |
| Lab 1 - Security Onion Setup.docx                  | Installation of Security Onion with Suricata and Wazuh deployment |
| Lab 2 - pfSense Firewall Configuration.docx        | Setup of pfSense firewall and syslog forwarding to Security Onion |
| Exercise4Scada(1).docx                             | Integration of Snort IDS in pfSense (including IPS mode setup)  |
| Lab 5 - Using Wazuh to add PowerShell logging.docx | Monitoring of PowerShell execution logs via Wazuh (Event ID 4104) |
| Lab 6 - Using Wazuh to add Sysmon logging.docx     | Configuration of Sysmon for enhanced endpoint telemetry          |
| Lab 7 - Creating pfSense Firewall Dashboard in Kibana.docx | Custom dashboard creation in Kibana for pfSense log analysis     |

---

## 🧱 Lab Architecture Overview

### Network Segments
- Internal Zone: `192.168.10.0/24`
- External Zone: `192.168.20.0/24`
- DMZ: `10.10.10.0/24`

### Virtual Machines
- Security Onion: Acts as IDS and SIEM using Suricata, Wazuh, and the ELK stack  
- pfSense: Serves as the primary firewall and Snort IDS/IPS host  
- Windows VM: Used for endpoint activity and logging (PowerShell, Sysmon)  

---

## 🔍 Lab Highlights

- Lab 0 – Virtual Network Setup: Creation of isolated NAT networks using VirtualBox for segmented environment simulation.
- Lab 1 – Security Onion: Deployment of Suricata and Wazuh on Security Onion; configuration of rule sets and host monitoring.
- Lab 2 – pfSense Firewall: Installation of pfSense; configuration of syslog forwarding to ELK for centralized monitoring.
- Lab 4 – Snort IDS Integration: Implementation of Snort on pfSense, including switching to IPS mode and verifying alerts via test patterns.
- Lab 5 – PowerShell Logging with Wazuh: Enablement of Event ID 4104 logging using Group Policy; forwarding of PowerShell events via Wazuh.
- Lab 6 – Sysmon Endpoint Logging: Deployment of Sysmon using the SwiftOnSecurity configuration; visibility into process, file, and network activity.
- Lab 7 – Kibana Dashboard: Creation of interactive Kibana visualizations including:
  - Source and destination IP summaries
  - Port and protocol tracking
  - Action-based log distributions (e.g., ALLOW/DENY)

---

## 🛠️ Tools & Technologies

- VirtualBox – Virtual machine and network isolation platform  
- Security Onion – Centralized threat detection using Suricata and Wazuh  
- pfSense – Open-source firewall solution supporting Snort IDS/IPS  
- Wazuh – Host-based intrusion detection and log forwarding tool  
- Sysmon – System monitoring tool for Windows endpoints  
- Kibana – Visualization and analysis dashboard for ELK stack logs

---

## 📄 License

This project is released under the  
Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)

> Usage and distribution are allowed with appropriate attribution. Modification and commercial use are not permitted.

🔗 [View Full License Terms](https://creativecommons.org/licenses/by-nc-nd/4.0/)
