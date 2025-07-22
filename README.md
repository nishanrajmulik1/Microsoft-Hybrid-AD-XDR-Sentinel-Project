# 🔐 Microsoft Hybrid AD + Microsoft XDR + Sentinel Detection Lab

![Status](https://img.shields.io/badge/status-completed-brightgreen)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Azure-lightgrey)

## 📌 Overview

This project demonstrates a hybrid identity and security monitoring setup using:

- 🧠 **Azure AD Connect** (Hybrid AD join)
- 🛡️ **Microsoft Defender for Endpoint (MDE)**
- 📊 **Microsoft Sentinel (SIEM)**
- ⚙️ **Microsoft Intune (MDM/MEM)**
- 🚨 **Microsoft XDR alerting**
- 💣 Simulated attack: **Mimikatz LSASS Memory Dump**

## 🎯 Objectives

- Connect on-premises AD to Azure AD using AD Connect
- Onboard Windows Server and Workstation to Defender for Endpoint
- Enable Microsoft Sentinel for centralised logging and incident management
- Use Intune for compliance and visibility
- Simulate credential dumping (Mimikatz) and detect it in Defender XDR and Sentinel

## 🏗️ Architecture

![Hybrid Lab Architecture](Architecture/ProjectArchitecture.jpeg)

## ⚙️ Configuration Steps

### ✅ Azure AD Connect Setup

![OnpremAD](Screenshots/OnpremAD.png)  
![EntraID](Screenshots/Entraconnect.png)

### ✅ Microsoft Defender for Endpoint Onboarding

![MicrosoftXDR](Screenshots/MicrosoftXDRalldevices.png)  
![XDROverview](Screenshots/MicrosoftDefenderDeviceInventory.png)

## 🧪 Attack Simulation

- Mimikatz used on on-prem Windows Server (`sekurlsa::logonPasswords`)
- Alert triggered in Microsoft Defender XDR
- Logs visible in Sentinel

### 📸 Defender XDR Alert on Domain Controller

- Alert Overview:  
  ![DCOverview](Screenshots/nishantechdcoverviewinxdr.png)

- Mimikatz Detected:  
  ![DCMimikatzDetected](Screenshots/dcmimikatzexecutedetected.png)

- Execution Timeline:  
  ![DCMimikatzexecution](Screenshots/dcmimikatzexecutiondetected.png)

- Process Tree:  
  ![DCmimikatzProcessTree](Screenshots/dcmimikatzprocesstree.png)

### 📸 Defender XDR Alert on Workstation WS02

- Alert Overview:  
  ![WS02Overview](Screenshots/WS02Overview.png)

- Mimikatz Detected:  
  ![WS02Mimikatzdetected](Screenshots/WS02mimikatzdetected.png)

- Threat Details:  
  ![WS02Mimikatzdetails](Screenshots/WS02mimikatzmalwaredetected.png)

### 📸 Sentinel Logs and Dashboard

- Mimikatz Logs in Sentinel:  
  ![Sentinel Mimikatz Logs](Screenshots/SentinelMimikatz.png)

- MDATP Logs in Sentinel:  
  ![Sentinel MDATP Logs](Screenshots/SentinelMDATP.png)

- Sentinel SOC Dashboard:  
  ![Dashboard](Screenshots/SOCdashboard.png)

## 🧠 Learning Outcomes

- Understanding of hybrid identity integration
- Hands-on with Microsoft XDR & SIEM
- Detection engineering basics (simulating & detecting attacks)
- Cloud-native threat response and visibility

## 🧰 Tools Used

| Tool | Role |
|------|------|
| Azure AD | Cloud identity |
| AD Connect | Sync on-prem AD |
| Microsoft Defender | Endpoint protection |
| Microsoft Sentinel | SIEM |
| Intune | MDM & policy enforcement |
| Mimikatz | Attack simulation |

---

## 🧵 Project Author

**Nishan Rajmulik**  
Cybersecurity Enthusiast | Blue Team Focus  
[LinkedIn](https://www.linkedin.com/in/nishanrajmulik)
