# 🔐 Microsoft Hybrid AD + Microsoft XDR + Sentinel Detection Lab

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

![Hybrid Lab Architecture](Architecture/hybrid_architecture_diagram.png)

## ⚙️ Configuration Steps

- ✅ Azure AD Connect Setup: [`Configurations/ad_connect_config.md`](Configurations/ad_connect_config.md)
- ✅ Microsoft Defender for Endpoint Onboarding: [`Configurations/defender_onboarding.md`](Configurations/defender_onboarding.md)
- ✅ Sentinel Rule Creation & Alerting: [`Configurations/sentinel_rules_alerts.md`](Configurations/sentinel_rules_alerts.md)

## 🧪 Attack Simulation

- Mimikatz used on on-prem Windows Server (`sekurlsa::logonPasswords`)
- Alert triggered in Microsoft Defender XDR
- Logs visible in Sentinel

📸 Screenshots:
- Defender XDR Alert: ![](Screenshots/xdr_alert.png)
- Sentinel Incident: ![](Screenshots/sentinel_incident.png)

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
Cybersecurity Enthusiast | Blue Team Focus | [LinkedIn](https://www.linkedin.com/in/nishanrajmulik)

