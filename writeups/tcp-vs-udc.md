# 🌐 TCP vs UDP

**Room:** TCP vs UDP
**Path:** Network Fundamentals
**Date:** 05 April 2026
**Difficulty:** Easy

---

## 🧠 Core Concept

Data transmission can follow two main transport protocols:

* 🔒 TCP (Reliable, connection-based with handshake)
* ⚡ UDP (Fast, connectionless — no handshake)

---

## 🔍 Definitions

### 🔒 TCP (Transmission Control Protocol)

* Connection-oriented (uses **3-way handshake**)
* Reliable delivery (guaranteed)
* Ordered data transmission
* Error checking & retransmission
* Slower but accurate

---

### ⚡ UDP (User Datagram Protocol)

* Connectionless (**no handshake**)
* No delivery guarantee
* No ordering of data
* Minimal error checking
* Faster but less reliable

---

## 🤝 TCP Handshake (Important)

TCP establishes a connection using a **3-step process**:

1. **SYN** → Client sends request
2. **SYN-ACK** → Server acknowledges
3. **ACK** → Client confirms

👉 Connection established before data transfer

---

## ⚔️ Key Differences

| Feature         | 🔒 TCP                    | ⚡ UDP                   |
| --------------- | ------------------------- | ----------------------- |
| Connection Type | Connection-oriented       | Connectionless          |
| Handshake       | ✅ 3-way handshake         | ❌ No handshake          |
| Reliability     | ✅ Guaranteed delivery     | ❌ No guarantee          |
| Speed           | Slower                    | Faster                  |
| Ordering        | ✅ Maintains order         | ❌ No order              |
| Error Handling  | ✅ Retransmission          | ❌ Minimal               |
| Overhead        | High                      | Low                     |
| Use Cases       | Web, Email, File Transfer | Streaming, Gaming, VoIP |

---

## 🔄 How Data Travels

### 🔒 TCP Flow:

1. Handshake (SYN → SYN-ACK → ACK)
2. Data sent in sequence
3. Acknowledgments received
4. Lost data retransmitted

### ⚡ UDP Flow:

1. Data sent instantly
2. No connection setup
3. No confirmation or resend

---

## 🧠 Memory Hook

👉 "TCP = Handshake then Talk, UDP = Just Talk"

* TCP = Connect first, then send
* UDP = Send immediately

---

## 🛡️ Why It Matters (SOC / Blue Team)

* Detect attacks like:

  * SYN flood (abuse of TCP handshake)
  * UDP flood (no connection needed)
* Analyze traffic behavior in Wireshark
* Spot incomplete or suspicious handshakes

---

## 🔥 Quick Recall

* TCP = Handshake + Reliable + Ordered
* UDP = No Handshake + Fast + Lightweight

---

**Status:** Completed ✅
