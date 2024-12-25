# Home Lab

Welcome to my **Home Lab** project!  
This setup serves as my personal network, designed with a focus on **security**, **networking**, and **educational purposes**. Below you'll find a breakdown of the components, their roles, and how everything fits together.

---

## **Overview**

The Home Lab is built to simulate a professional network environment while maintaining simplicity and cost-efficiency. It includes hardware and virtual machines (VMs) running essential services for managing and monitoring the network. The lab also supports practical security challenges and experiments.

---

## **Components**

### **1. ISP Router**
`Gateway`  
Acts as the gateway to the internet and the first layer of protection for the home network.

---

### **2. Mini PC HP**  
`Virtualization` `Proxmox`  
- **Specifications:** Intel Core i3, 16 GB RAM (upgraded from 8 GB), 500 GB HDD + 128 GB SSD  
- **Operating System:** Proxmox VE (Virtualization Environment)

#### **Virtual Machines (VMs):**  
- **pfSense:**  
   `Firewall` `Router`  
  - **Role:** Router and firewall for internal network management.  
  - **Features:** Firewall rules, NAT, and VLAN management.

- **Windows Server 2016:**  
  `AD` `DNS` `DHCP`  
  - **Role:** Provides Active Directory (AD), DNS, and DHCP services.  
  - **Use Case:** Domain controller for centralized user and device management.

- **Kali Linux:**  
  `Pen-testing` `Security`  
  - **Role:** A pen-testing environment.  
  - **Use Case:** Participating in security challenges (e.g., Try Hack Me).  

- **Linux Server:**  
  `Docker` `Containers`  
  - **Role:** Docker host for containerized applications.  
  - **Containers include:**  
    - **Zabbix:**  
      - **Tag:** `Monitoring`  
      - **Role:** Network and system monitoring.  
    - **Suricata:**  
      - **Tag:** `IDS` `Security`  
      - **Role:** Intrusion Detection System (IDS).  

---

### **3. Windows 10 Pro**
`Workstation`  
- **Role:** Main workstation for daily activities.  
- **Use Case:** Accessing VMs, network resources, and administrative tasks.

---

### **4. Raspberry Pi Devices**

- **Raspberry Pi 8 GB:**  
  `File Management` `Automation`  
  - **Operating System:** Ubuntu Server with CasaOS.  
  - **Role:** Centralized file management and home automation.

- **Raspberry Pi 2 GB:**  
  `Vulnerability Management`  
  - **Operating System:** Ubuntu Server.  
  - **Role:** Runs Nessus for vulnerability scanning and management.

---

### **5. TP-Link TL-SG10E**  
`VLAN` `Network Segmentation`  
- **Role:** Smart switch for logical network segmentation using VLANs.  
- **Use Case:** Isolating different parts of the network for enhanced security.

---

## **Features**

- **Logical Network Segmentation:**  
  `VLAN`  
  - VLANs implemented via pfSense and TP-Link smart switch to ensure separation between devices and services (e.g., IoT, servers, workstations).

- **Network Monitoring:**  
   `Monitoring` `IDS`  
  - Zabbix and Suricata provide real-time monitoring, alerting, and threat detection.

- **Vulnerability Management:**  
  `Vulnerability Scanning`  
  - Nessus scans the network for vulnerabilities to ensure a secure environment.

- **Penetration Testing Environment:**  
   `Pen-testing`  
  - Kali Linux VM for practicing ethical hacking and security challenges.

- **Home Automation and File Management:**  
  `CasaOS` `File Sharing`  
  - CasaOS on Raspberry Pi 8 GB for organizing and accessing files seamlessly.

---

## **Goals**

1. **Learn and implement key networking concepts:**  
   `Firewall` `VLAN` `DNS` `DHCP`
2. **Improve understanding of security:**  
   `IDS` `Pen-testing` `Vulnerability Scanning`
3. **Gain practical experience with virtualized environments:**  
   `Proxmox` `Docker` `Containers`

---

## **Usage**

1. **Access Proxmox Dashboard:**  
   Manage and monitor VMs using the Proxmox web interface.  

2. **Connect to pfSense:**  
   Control routing and firewall settings via the pfSense interface.  
    
3. **Workstation Access:**  
   Use Windows 10 Pro to remotely manage VMs and containers.   

4. **Network Monitoring:**  
   Utilize Zabbix for detailed monitoring and Suricata for intrusion detection alerts.   

5. **File Sharing and Automation:**  
   Access shared files via CasaOS and Raspberry Pi.   

---

## **Future Plans**

- Implement Proxmox Backup Server for automated VM snapshots.  
- Expand the homelab with new tools and services (e.g., Plex Media Server, GitLab).  
- Explore clustering in Docker for high availability.  
- **Tags:** `Backup` `Expansion` `Clustering`

---

## **Acknowledgments**

This Home Lab project was inspired by a desire to learn and grow in the fields of networking, virtualization, and cybersecurity.
