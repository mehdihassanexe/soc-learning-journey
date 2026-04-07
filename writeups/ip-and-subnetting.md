# THM - IP Addressing & Subnetting

**Room:** IP Addressing & Subnetting
**Path:** Network Fundamentals
**Date:** 07 April 2026
**Difficulty:** Medium

---

## What I Learned

* Every device on a network needs a unique **IP address** to communicate.

* An IP address is divided into:

  * **Network portion** → identifies the network
  * **Host portion** → identifies the device

* Two types of IP addresses:

  * **IPv4** → 32-bit (e.g., 192.168.1.10)
  * **IPv6** → 128-bit (used for future scalability)

---

## Subnetting Basics

* **Subnetting** = dividing one large network into smaller networks.

* It is used to:

  * Improve security
  * Reduce broadcast traffic
  * Optimize IP usage

* A **Subnet Mask** defines which part is network vs host.

Example:

```
IP Address: 192.168.1.10  
Subnet Mask: 255.255.255.0 (/24)

Network → 192.168.1  
Host → .10
```

---

## Key Concepts

### Private IP Ranges

* 10.0.0.0 – 10.255.255.255
* 172.16.0.0 – 172.31.255.255
* 192.168.0.0 – 192.168.255.255

👉 Used inside networks (not routable on the internet)

---

### CIDR Notation

* Short form of subnet mask
* Example:

  * /24 = 255.255.255.0
  * /26 = 255.255.255.192

---

## Subnetting Rules (Easy Memory Version)

### 1. Block Size Formula

```
Block Size = 256 - Last Octet of Subnet Mask
```

Example:

```
/26 → 255.255.255.192  
256 - 192 = 64
```

---

### 2. CIDR Quick Table (Must Memorize)

| CIDR | Block Size | Usable Hosts |
| ---- | ---------- | ------------ |
| /24  | 256        | 254          |
| /25  | 128        | 126          |
| /26  | 64         | 62           |
| /27  | 32         | 30           |
| /28  | 16         | 14           |
| /29  | 8          | 6            |
| /30  | 4          | 2            |

👉 Pattern: **Divide block size by 2 each step**

---

### 3. Always Remember

* First IP → **Network Address** ❌
* Last IP → **Broadcast Address** ❌
* Remaining → **Usable Hosts** ✅

---

## Example

```
IP: 192.168.1.70  
Mask: /26
```

Step 1: Block Size

```
256 - 192 = 64
```

Step 2: Ranges

```
0–63  
64–127  ← IP is here  
128–191  
192–255  
```

Step 3: Identify

```
Network:   192.168.1.64  
Broadcast: 192.168.1.127  
Usable:    192.168.1.65 – 192.168.1.126  
```

---

## Memory Hook

> **IP Address = Street Address**
> **Subnet Mask = Street vs House divider**

OR

> “Find block size → jump ranges → locate network → exclude first & last”

---

## Why It Matters for SOC / Blue Team

* Helps identify **network segmentation**
* Detects **lateral movement between subnets**
* Important for:

  * Firewall rules
  * Access Control Lists (ACLs)
  * Log analysis (internal vs external traffic)

Example:

```
192.168.1.10 → 192.168.2.15
```

👉 Different subnets → possible lateral movement

---

## Final Quick Revision

```
/24 = 256  
/25 = 128  
/26 = 64  
/27 = 32  
/28 = 16  
/29 = 8  
/30 = 4  
```

👉 Just keep dividing by 2

---

**Status:** Completed ✅
