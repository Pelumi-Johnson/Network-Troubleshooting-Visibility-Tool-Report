# 🔍 Network Troubleshooting & Visibility Tool Report

 📄 **Full Lab Report:**  
👉 [Click here to open the complete lab report](https://github.com/Pelumi-Johnson/Network-Troubleshooting-Visibility-Tool-Report/blob/main/TroubleshootingAndToolReportTemplate_Edited.pdf)

---

### 🧰 Detecting Inbound Network Activity Using Netstat
Hands-on troubleshooting project focused on identifying and analyzing inbound network connection attempts using the `netstat` utility to determine whether adversaries or unauthorized services are reaching internal systems.

---

## 🎯 Project Objective
The objective of this project was to determine **whether inbound connection requests were legitimate or potentially hostile**, and to identify which **ports, protocols, and processes** were involved.

This mirrors real-world scenarios where IT or security teams must quickly gain visibility into network activity to detect reconnaissance, misconfigurations, or early-stage intrusion attempts.

---

## 🧩 Network Problem Identified
After establishing an internet connection, **unexpected inbound connection attempts** were observed.

Key concerns:
- Are external systems attempting to reach internal hosts?
- Which ports and protocols are exposed?
- Are any services running that should not be publicly accessible?

---

## 🛠️ Tool Selected: Netstat
**Netstat** is a built-in Windows and Linux utility used to display:
- Active network connections
- Listening ports
- Protocols in use
- Process IDs (PIDs)
- Foreign (remote) IP addresses

Netstat provides immediate visibility into **who is connected**, **how**, and **through which services**, making it ideal for early investigation and situational awareness :contentReference[oaicite:0]{index=0}.

---

## 🧠 Troubleshooting Methodology Applied

### 1️⃣ Identify the Problem
- Reviewed alerts indicating inbound traffic
- Confirmed affected systems
- Noted source IPs and ports involved

### 2️⃣ Establish a Theory of Probable Cause
- Legitimate remote services
- Misconfigured or unnecessary open ports
- External scanning or reconnaissance activity

### 3️⃣ Test the Theory
Used `netstat` to inspect:
- Active connections
- Listening services
- Unknown or suspicious foreign addresses

### 4️⃣ Establish a Plan of Action
If hostile or unnecessary traffic is confirmed:
- Block suspicious IP addresses
- Disable unneeded services
- Harden firewall rules
- Isolate affected hosts if required

### 5️⃣ Implement the Solution
- Applied filtering or service configuration changes
- Closed unnecessary ports
- Re-ran netstat to validate changes

### 6️⃣ Verify Full System Functionality
- Ensured essential services remained operational
- Confirmed no abnormal inbound activity persisted

### 7️⃣ Document Findings
- Recorded observed traffic patterns
- Logged tools and commands used
- Noted remediation actions for future reference

---

## ⚙️ Netstat Command Usage

- `netstat -a`  
  Displays all active connections and listening ports

- `netstat -n`  
  Shows numerical IP addresses for easier analysis

- `netstat -o`  
  Displays process IDs associated with connections

- `netstat -an`  
  Combines active connections with numeric output

- `netstat -b` *(Windows)*  
  Shows which executable created each connection

- `netstat -r`  
  Displays routing table information

---

## 🧠 Key Takeaways
- Open ports equal potential exposure
- Visibility is the first step in defense
- Netstat provides fast, low-level insight during investigations
- Small misconfigurations can create unnecessary risk if left unchecked

This exercise reinforced the importance of **monitoring before reacting** and **verifying before blocking**.

