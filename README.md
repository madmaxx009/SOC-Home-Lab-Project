# SOC-Home-Lab-Project

## Description
This project demonstrates a Security Operations Center (SOC) home lab environment designed to simulate real-world cyberattacks and detection capabilities using Splunk. The lab includes log forwarding, attack simulation, and alert generation to showcase security monitoring and incident detection.


## Lab Overview
The setup includes three virtual machines:

1.Attacker Machine: Kali Linux

2.Target Machine: Ubuntu  (vulnerable web app, SSH, FTP)

3.SIEM Server: Windows with Splunk Enterprise


## Technologies Used

*Splunk Enterprise (Windows)

*Splunk Universal Forwarder (Ubuntu)

*Kali Linux (Attack simulation)

*VirtualBox or any hypervisor

*Apache2, vsftpd, custom login page

## Setup Steps

1.Configure Ubuntu (Target)
   *Install Apache, FTP, and a custom vulnerable login page.
  
   *Install and configure Splunk Universal Forwarder.
  
   * Forward /var/log/auth.log and /var/log/apache2/* to the Splunk server.
   
2.Configure Splunk Server (Windows)
   *Install Splunk Enterprise.
  
   *Configure inputs for receiving logs from forwarder.
 
   *Create dashboards and alerts.
   
3.Launch Attacks from Kali
  *SSH brute-force using hydra
  
  *Web login brute-force using hydra or wfuzz

  *Web directory enumeration using gobuster

  *FTP anonymous login attempts
 
  *Trigger Windows failed logins manually for detection


## Alerts Configured
*SSH Brute Force Detection

*Web Login Brute Force Detection

*Web Directory Enumeration

*FTP Anonymous Login Detection

*Windows Failed Login Attempts (EventCode 4625)

Each alert is created in Splunk using search queries that detect suspicious behavior and generate visual insights for security analysis.

## Screenshots

![Screenshot 2025-05-20 102945](https://github.com/user-attachments/assets/c71a50e9-2e76-4046-a109-0f21e4b4d040)

![Screenshot 2025-05-20 102913](https://github.com/user-attachments/assets/3ae26b0e-ef43-476c-a0ec-46f6602f6bfe)

![Screenshot 2025-05-20 101105](https://github.com/user-attachments/assets/2b052128-cbab-48bc-8a8e-94e0558e94a4)


## Learning Outcomes

*Gained hands-on experience with log forwarding and SIEM configuration.

*Simulated real-world attacks to test detection capabilities.

*Built proactive alerts and dashboards in Splunk.

## Future Improvements

Add ELK Stack version
Integrate Suricata/Zeek for packet-level detection
Automate log parsing with custom props and transforms
  
