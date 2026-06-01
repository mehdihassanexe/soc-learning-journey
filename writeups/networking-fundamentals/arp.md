# ARP (Address Resolution Protocol)

**Room:** ARP  
**Path:** Network Essentials  
**Date:** 1 June 2026  
**Difficulty:** Easy  

## Core Concept

ARP is used to find the **MAC address** of a device when its **IP address** is known.

Devices communicate using IP addresses, but Ethernet and Wi-Fi frames are delivered using MAC addresses.

Before sending data on a local network, a device must discover the destination MAC address.

---

## Why ARP Is Needed

Suppose your computer wants to send data to:

```text
192.168.1.1
```

Your computer knows the IP address but does not know the MAC address.

ARP helps answer:

> "Who has IP address 192.168.1.1?"

The device with that IP replies with its MAC address.

---

## Definitions

### ARP Request

A broadcast message sent to all devices on the local network.

Purpose:

> "Who has this IP address?"

Destination MAC:

```text
ff:ff:ff:ff:ff:ff
```

(Broadcast MAC address)

---

### ARP Reply

A unicast response sent back to the requester.

Purpose:

> "I have that IP address. Here is my MAC address."

Example:

```text
192.168.1.1 is at 44:df:65:d8:fe:6c
```

---

## ARP Process

### Step 1: Device Knows IP

Computer wants to contact:

```text
192.168.1.1
```

But MAC address is unknown.

---

### Step 2: ARP Request

Computer broadcasts:

```text
Who has 192.168.1.1?
Tell 192.168.1.100
```

Every device on the network receives the request.

---

### Step 3: ARP Reply

The correct device responds:

```text
192.168.1.1 is at 44:df:65:d8:fe:6c
```

---

### Step 4: Communication Begins

The sender stores the MAC address in its ARP cache.

It can now send Ethernet frames directly to the destination.

---

## Memory Hook

Think:

```text
IP Address = Person's Name
MAC Address = Home Address
ARP = Address Book Lookup
```

Or:

```text
Know IP
Ask ARP
Get MAC
Send Data
```

---

## Important Fact

ARP does **NOT** use IP packets.

ARP is carried directly inside an Ethernet frame.

Normal communication:

```text
Ethernet Frame
 └─ IP Packet
     └─ Data
```

ARP communication:

```text
Ethernet Frame
 └─ ARP Message
```

No IP packet is involved.

---

## Broadcast MAC Address

ARP Requests use:

```text
ff:ff:ff:ff:ff:ff
```

Meaning:

> "Send this to everyone on the local network."

Only the device owning the requested IP address replies.

---

## Why It Matters (SOC / Blue Team)

ARP helps analysts:

- Identify devices on a network
- Detect ARP spoofing attacks
- Investigate man-in-the-middle attacks
- Monitor device communication
- Troubleshoot connectivity issues

---

## Quick Recall

- ARP = Address Resolution Protocol
- Converts IP addresses into MAC addresses
- ARP Request = Broadcast
- ARP Reply = Unicast
- Used only on local networks
- Works directly over Ethernet
- Uses MAC address `ff:ff:ff:ff:ff:ff` for broadcasts

---

## One-Line Summary

ARP (Address Resolution Protocol) resolves an IP address to a MAC address by sending a broadcast ARP Request and receiving a unicast ARP Reply.

**Status: Completed ✅**
