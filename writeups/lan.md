# Local Area Network (LAN)

**Date:** 31 March 2026  
**Module:** Networking Fundamentals  

---

## 📌 Key Points

- A **Local Area Network (LAN)** is a network that connects devices within a limited geographic area (home, office, school).
- Common LAN technologies include:
  - **Ethernet** (wired)
  - **Wi-Fi** (wireless)
- Devices in a LAN can include:
  - Computers
  - Servers
  - Printers
  - Switches
  - Routers
- LANs typically use private IP address ranges:
  - `192.168.x.x`
  - `10.x.x.x`
- A **switch**:
  - Connects devices within the LAN
  - Forwards data based on MAC addresses
- A **router**:
  - Connects the LAN to external networks (e.g., the internet)
- LAN communication uses protocols such as:
  - **TCP/IP**
  - **ARP**
  - **DHCP**
- **DHCP** automatically assigns IP addresses to devices.
- **ARP** maps IP addresses to MAC addresses within the LAN.
- LANs provide:
  - High-speed communication
  - Low latency compared to WANs
- Security risks include:
  - Unauthorized access
  - ARP spoofing
  - Lateral movement by attackers
- **VLANs (Virtual LANs)**:
  - Segment networks logically
  - Improve security and management

---

## 🧠 Memory Hook

> **LAN = Local, Fast, and Close**  
> *(Devices talking in the same room)*

---

## 🛡️ Why It Matters for SOC

- Helps analysts understand:
  - Internal traffic patterns vs external threats
- Critical for detecting:
  - **Lateral movement** (attackers spreading inside a network)
- Enables identification of suspicious behavior such as:
  - Unusual ARP requests *(possible spoofing)*
  - Unauthorized devices joining the network
  - Abnormal internal scanning activity
- Common log sources tied to LAN activity:
  - Firewall logs
  - Switch logs
  - Endpoint logs
- Helps in:
  - **Incident scoping** (which systems are affected)
- VLAN knowledge helps:
  - Trace attacks across segmented environments

---

## ❓ Questions / Confusions

- How does ARP spoofing get detected in real-world SOC tools?
- What logs best show lateral movement inside a LAN?
- What is the difference between managed vs unmanaged switches in security monitoring?

---

## 📊 Status

**Needs Review**
