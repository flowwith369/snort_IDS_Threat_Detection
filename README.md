
# Snort IDS/IPS Lab Implementation

A hands-on implementation of Snort as an Intrusion Detection System (IDS) 
and Intrusion Prevention System (IPS) on Kali Linux, demonstrating 
real-time network traffic monitoring and custom rule-based alert generation.

---

## 🎯 Objective

To configure Snort to monitor live network traffic, write custom detection 
rules, generate alerts for suspicious activity, and analyze the results — 
simulating a real-world network security monitoring scenario.

---

## 🛠️ Tools & Environment

- **OS:** Kali Linux
- **Tool:** Snort++ 3.12.1.0
- **Interface:** eth0
- **Protocol Tested:** ICMP (Ping)

---

## 📋 What This Lab Covers

- Installing and verifying Snort on Kali Linux
- Configuring network interface using ifconfig
- Writing a custom Snort rule to detect ICMP traffic
- Updating snort.lua configuration to include local rules
- Running Snort in IDS mode and generating real-time alerts
- Analyzing alert logs with timestamp, source & destination IPs

---

## 🔍 Custom Rule Used

```bash
alert icmp any any -> any any (msg:"Ping Detected"; sid:1000001; rev:1;)
```

This rule detects all ICMP (ping) traffic on the network and generates 
an alert with the message "Ping Detected".

---

## ✅ Result

Snort successfully detected ICMP packets in real time, generating timestamped 
alerts showing source and destination IP addresses — confirming the IDS 
was functioning correctly.

---

## 📄 Full Lab Report

The detailed lab report with screenshots and step-by-step explanation 
is available in the file:

👉 [`Snort lab.pdf`](Snort lab.pdf)

---

## 📚 Key Learnings

- Difference between IDS (detect & alert) vs IPS (detect & block)
- Snort rule structure: Rule Header vs Rule Options
- How packet-level analysis works using predefined signatures
- Real-time traffic monitoring on a live network interface

---

## 👤 Author

**Nagati Upendar**  
M.Sc Cybersecurity & Digital Forensics | Penetration Tester | VAPT  
📧 upendar0369@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/upendar-x369)
