# THM Room: HTTP in Detail

**Date:** 29 March 2026  
**Path:** Pre Security / How The Web Works  
**Difficulty:** Easy

## What I Learned

- HTTP stands for Hypertext Transfer Protocol and is used for communication between web browsers and servers.
- HTTP is **stateless** — the server does not remember previous requests.
- State is maintained using **cookies** and **session IDs** so websites can remember logged-in users.
- Main HTTP Methods:
  - **GET** → Retrieve data (used when loading a webpage)
  - **POST** → Send data to the server (used for login forms, uploading files, etc.)

## Hands-on Practice

- Used Firefox Developer Tools (F12 → Network tab)
- Reloaded a page and inspected real GET requests
- Observed important fields:
  - **Scheme**: http or https
  - **Host**: Server name (e.g. httpdemo.local)
  - **Path**: Requested file ("/" usually means index.html)
  - **Status Code**: 200 OK = successful request
  - **Response Body**: Contains the actual HTML content

## Why This Matters for SOC / Blue Team

- Understanding HTTP helps in analyzing web traffic in logs
- Useful for detecting suspicious GET/POST requests during investigations
- Foundation for later topics like web attacks, Burp Suite, and log analysis

## Key Takeaway
HTTP itself has no memory (stateless), but cookies and sessions make websites feel "remembered".

---

**Status:** Completed ✅
