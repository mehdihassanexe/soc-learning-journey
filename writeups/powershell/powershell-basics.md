# PowerShell Practice Notes

**Room:** PowerShell
**Path:** CyberSecurity 101/Command Line 
**Date:** 19 May 2026  
**Difficulty:** Easy

---

## 📁 Getting Files and Folders

List files and directories in the current location:
```powershell
Get-ChildItem
````

---

## 🔍 Filtering Files

Filter only `.txt` files:

```powershell
Get-ChildItem | Where-Object {$_.Extension -eq ".txt"}
```

Shorter version:

```powershell
Get-ChildItem | Where-Object Extension -EQ ".txt"
```

---

## 📌 Selecting Properties

Select specific properties of files:

```powershell
Get-ChildItem | Select-Object Name, Extension, Length
```

Using explicit property flag:

```powershell
Get-ChildItem | Select-Object -Property Name, Extension, Length
```

---

## 📂 Working with Folders

Create a folder:

```powershell
New-Item -ItemType Directory -Path .\foldername
```

Rename a folder:

```powershell
Rename-Item .\oldname newname
```

---

## 🔎 Searching Files in a Parent Directory

Search inside a folder and subfolders:

```powershell
Get-ChildItem -Path .\writeups -Recurse
```

Filter by name:

```powershell
Get-ChildItem -Path .\writeups -Recurse | Where-Object Name -like "*cia*"
```

Filter by file type:

```powershell
Get-ChildItem -Path .\writeups -Recurse -Filter *.md
```

---

## 🧠 Searching Inside Files

Search for text inside files:

```powershell
Select-String -Path .\writeups\* -Pattern "CIA"
```

Recursive search:

```powershell
Get-ChildItem .\writeups -Recurse -Filter *.md | Select-String "CIA"
```
---

## 🧠 Systems & Network Information

Retrieve comprehensive system information:
```powershell
Get-ComputerInfo
```
Lists all the local user accounts on the system:
```powershell
Get-LocalUser
```
Retrieve detailed information about the network interfaces on the system, including IP addresses, DNS servers, and gateway configurations:
```powershell
Get-NetIPConfiguration
```
Retrieve details for all IP addresses configured on the system, including those that are not currently active.
```powershell
Get-NetIPAddress
```
---

## 📌 Notes

* `Get-ChildItem` → list files
* `Where-Object` → filter results
* `Select-Object` → choose properties
* `Select-String` → search inside file content
* `-Recurse` → include subfolders

---

## 🚀 Summary

These commands cover basic file navigation, filtering, searching & retrieving system/network info in PowerShell for beginners.

```.
```

