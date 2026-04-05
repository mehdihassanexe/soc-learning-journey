# 📦 Packets & Frames

**Room:** Packets & Frames  
**Path:** Network Fundamentals  
**Date:** April 2026  
**Difficulty:** Easy

---

## 🧠 Core Concept

Data doesn’t travel as one big chunk — it’s broken down into:

- 🧩 Packets (Layer 3 – Network)
- 📨 Frames (Layer 2 – Data Link)

---

## 🔍 Definitions

### 📨 Frame (Layer 2)
- Uses MAC Addresses (physical address)
- Works within a LAN (Local Network)
- Includes Error Checking (CRC)
- Stops at the Router

---

### 🧩 Packet (Layer 3)
- Uses IP Addresses (logical address)
- Travels across multiple networks
- Routed via Routers
- Contains data + headers

---

## ⚔️ Key Differences

Feature            | 📨 Frame                  | 🧩 Packet
------------------|--------------------------|--------------------------
Layer             | 2 (Data Link)            | 3 (Network)
Address Type      | MAC Address              | IP Address
Scope             | Local Network (LAN)      | Across Networks
Router Behavior   | ❌ Stops at router       | ✅ Passes through routers
Error Handling    | ✅ CRC                   | ❌ No CRC

---

## 🔄 How Data Travels

1. Data is created  
2. Wrapped into a Packet (IP added)  
3. Encapsulated into a Frame (MAC added)  
4. Sent over network  
5. Decapsulation (Frame → Packet → Data)

---

## 🧠 Memory Hook

👉 "Frame = Local, Packet = Postal"

- Frame = Local delivery (MAC, same network)
- Packet = Postal system (IP, across networks)

---

## 🛡️ Why It Matters (SOC / Blue Team)

- Analyze traffic in Wireshark
- Spot anomalies:
  - Strange MAC/IP combos
  - Unusual packet sizes
- Understand attack movement

---

## 🔥 Quick Recall

- Frame = Layer 2 + MAC + Local  
- Packet = Layer 3 + IP + Routing
  
---

**Status:** Completed ✅
