# Routing Protocols

**Room:** Networking Essentials  
**Platform:** TryHackMe  
**Path:** Cyber Security 101 → Networking  
**Module:** Routing Protocols  
**Date Studied:** 31 July 2026  
**Difficulty:** Easy

---

## Core Concept

Routing protocols allow routers to exchange information about networks and determine the best path for forwarding packets. Without routing protocols, routers would not know how to reach networks beyond their directly connected ones.

---

## What is Routing?

Routing is the process of selecting the best path for data to travel from a source network to a destination network.

Routers build and maintain **routing tables**, which contain information about reachable networks and the best next hop.

---

## Why Routing Protocols Are Needed

Imagine several networks connected together.

```text
Network A ─ Router ─ Router ─ Router ─ Network B
```

Each router must decide:

> "Which interface should I send this packet through?"

Routing protocols automate this decision by allowing routers to share network information.

---

# OSPF (Open Shortest Path First)

## Core Concept

OSPF is an **open standard link-state routing protocol** used within a single organization (Autonomous System). Every router builds a complete map of the network and calculates the shortest path to every destination.

### Characteristics

- Open standard
- Link-State Protocol
- Fast convergence
- Scalable
- Uses Dijkstra's Shortest Path First (SPF) algorithm

### Advantages

- Very fast
- Efficient in large networks
- Automatically recalculates routes after failures

### Best Used

- Enterprise networks
- Medium to large organizations

---

# EIGRP (Enhanced Interior Gateway Routing Protocol)

## Core Concept

EIGRP is a **Cisco-developed routing protocol** that combines characteristics of distance-vector and link-state routing. It selects routes based on metrics such as bandwidth and delay.

### Characteristics

- Cisco-developed protocol
- Fast convergence
- Uses multiple metrics
- Supports unequal-cost load balancing

### Metrics Used

- Bandwidth
- Delay
- Reliability
- Load (optional)

### Advantages

- Very efficient
- Quick route updates
- Excellent performance on Cisco equipment

### Best Used

- Cisco-based enterprise networks

### Exam Tip

✅ **Cisco proprietary protocol = EIGRP**

---

# BGP (Border Gateway Protocol)

## Core Concept

BGP is the routing protocol that powers the Internet. It exchanges routing information between different Autonomous Systems (AS), such as Internet Service Providers (ISPs), cloud providers, and large organizations.

### Characteristics

- Exterior Gateway Protocol (EGP)
- Internet's primary routing protocol
- Policy-based routing
- Highly scalable

### Advantages

- Supports millions of routes
- Highly reliable
- Controls Internet traffic between organizations

### Best Used

- ISPs
- Cloud providers
- Large enterprises

### Remember

**BGP = Internet Routing**

---

# RIP (Routing Information Protocol)

## Core Concept

RIP is one of the oldest and simplest routing protocols. It selects routes based solely on the number of hops between routers.

### Characteristics

- Distance Vector Protocol
- Maximum hop count: 15
- Slow convergence
- Easy to configure

### Metric

- Hop Count

### Advantages

- Very simple
- Easy to learn
- Suitable for small networks

### Limitations

- Not scalable
- Slow updates
- Inefficient for large networks

### Best Used

- Small LANs
- Learning environments

---

## Comparison

| Protocol | Type | Metric | Typical Use |
|----------|------|--------|-------------|
| OSPF | Link-State | Cost (Shortest Path) | Enterprise Networks |
| EIGRP | Advanced Distance Vector | Bandwidth, Delay, Reliability | Cisco Networks |
| BGP | Path Vector | Policies & AS Path | Internet Routing |
| RIP | Distance Vector | Hop Count | Small Networks |

---

## Memory Hooks

### OSPF

**Open = Open Standard**

Think:

> Builds a complete map of the network.

---

### EIGRP

**E = Enhanced Cisco Routing**

Think:

> Cisco's routing protocol.

---

### BGP

Think:

> **Backbone of the Internet**

Used between ISPs and large organizations.

---

### RIP

Think:

> **Counts hops only.**

Fewest hops wins.

---

## Why It Matters (SOC / Blue Team)

Understanding routing protocols helps analysts:

- Troubleshoot connectivity issues
- Investigate network outages
- Analyze packet paths
- Detect routing misconfigurations
- Understand network infrastructure during incident response

---

## Quick Recall

- Routing protocols help routers find the best path.
- OSPF = Link-State, shortest path.
- EIGRP = Cisco-developed routing protocol.
- BGP = Internet routing protocol.
- RIP = Chooses routes with the fewest hops.

---

## One-Line Summary

**Routing protocols allow routers to exchange network information and automatically determine the best path for forwarding packets across networks.**

---

**Status:** Completed ✅
