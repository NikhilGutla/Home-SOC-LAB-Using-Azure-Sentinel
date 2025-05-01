# Home-SOC-LAB-Using-Azure-Sentinel

This project demonstrates a cloud-based honeypot setup in Microsoft Azure to simulate real-world cyberattacks and analyze malicious behavior. By intentionally exposing a Windows 11 Pro virtual machine to the internet, I captured over 50,000+ attack attempts in under 6 hours and used Azure Sentinel and Log Analytics Workspace (LAW) to monitor, visualize, and interpret those threats. The objective was to gain hands-on experience in cloud security, SIEM operations, and threat intelligence using Microsoft’s security tools.

Architecture & Resources Used:

Azure Resource Group: Centralized management of all deployed components.
Virtual Network (VNet) & NSG: Custom inbound rule to allow all ports and protocols to simulate a vulnerable endpoint.
Windows 11 Pro VM: Deployed and firewall disabled to attract malicious traffic.
Log Analytics Workspace: Collected security events using the WindowsEvent extension.
Microsoft Sentinel: Integrated with LAW to build dashboards, query logs using KQL, and visualize attack sources via a custom workbook.
Sentinel Watchlist: Imported a geoip-summarized.csv file to enrich logs with geolocation data.
Attack Map: Created a custom Sentinel Workbook with a JSON-based visualization to map source locations of IP-based intrusion attempts.

Key Results
![Image](https://github.com/user-attachments/assets/276e906b-7152-49fb-92f4-7379ba33f3ea)
Captured over 50,000+ malicious requests including brute-force login attempts and automated scanning.
Used Kusto Query Language (KQL) to filter events (Event ID 4625) and correlate them with geo-IP data.
Visualized live attack trends on an interactive map to understand attacker behavior patterns.
