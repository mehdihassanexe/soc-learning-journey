# THM - DNS in Detail

**Room:** DNS in Detail  
**Path:** Network Fundamentals  
**Date:** 12 April 2026  
**Difficulty:** Easy

## What I Learned

- DNS stands for **Domain Name System** (not Server).
- DNS translates human-readable domain names (like google.com) into machine-readable **IP addresses** (like 142.250.190.78).
- Without DNS, we would have to remember IP addresses for every website.

## How DNS Works (Basic Flow)

1. User types a website name (e.g., google.com)
2. Computer checks its local DNS cache
3. If not found, it asks a DNS resolver (Recursive server)
4. Resolver queries Root server → TLD server → Authoritative server
5. IP address is returned and the website loads

## Important DNS Record Types

- **A Record** → Maps domain to IPv4 address
- **AAAA Record** → Maps domain to IPv6 address
- **CNAME** → Alias (one name points to another name)
- **MX** → Used for email servers

## Memory Hook

"DNS = Phonebook of the Internet"

## Why It Matters for SOC / Blue Team

- Many attacks use DNS (DNS Tunneling, DNS Spoofing, Command & Control)
- Suspicious DNS queries can indicate malware communication
- Important to monitor DNS logs during incident response

**Status:** Completed ✅
