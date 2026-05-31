# DHCP (Dynamic Host Configuration Protocol)

**Room:** DHCP  
**Path:** Network Essentials  
**Date:** 31 May 2026  
**Difficulty:** Easy

---

## Core Concept

DHCP automatically gives devices the network settings they need to communicate.

Instead of manually configuring every device, DHCP assigns:

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

Without DHCP, every device would need these settings entered manually.

---

## Definitions

### DHCP Server

A device that assigns network settings to clients.

Usually:

- Router
- Windows/Linux Server

Responsibilities:

- Maintains a pool of available IP addresses
- Assigns IP addresses
- Prevents IP conflicts

### DHCP Client

A device requesting network settings.

Examples:

- PC
- Laptop
- Phone
- Printer

---

## DORA Process

DHCP uses a four-step process:

### 1. Discover

Client asks:

> "Is there a DHCP server available?"

### 2. Offer

Server replies:

> "I can give you this IP address."

### 3. Request

Client responds:

> "I would like to use that address."

### 4. Acknowledge (ACK)

Server confirms:

> "Approved. You can use it."

The device can now communicate on the network.

---

## Memory Hook

**DORA**

- D = Discover
- O = Offer
- R = Request
- A = Acknowledge

Think:

**Ask → Offer → Accept → Confirm**

---

## Ports Used

| Device | Port |
|----------|------|
| DHCP Server | UDP 67 |
| DHCP Client | UDP 68 |

DHCP uses **UDP**, not TCP.

---

## Why It Matters (SOC / Blue Team)

DHCP helps analysts:

- Track devices joining the network
- Identify unauthorized devices
- Detect rogue DHCP servers
- Investigate IP conflicts
- Analyze DHCP traffic

---

## Quick Recall

- DHCP = Automatic IP assignment
- Uses UDP ports 67 and 68
- Process = DORA
- Assigns:
  - IP Address
  - Subnet Mask
  - Default Gateway
  - DNS Server

---

## One-Line Summary

**DHCP automatically assigns IP addresses and network settings using the DORA process.**

---

**Status:** Completed ✅
