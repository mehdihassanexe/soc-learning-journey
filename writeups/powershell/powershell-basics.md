````
# PowerShell Practice Notes

This document contains basic PowerShell commands practiced for file navigation, filtering, and searching.

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

## 📌 Notes

* `Get-ChildItem` → list files
* `Where-Object` → filter results
* `Select-Object` → choose properties
* `Select-String` → search inside file content
* `-Recurse` → include subfolders

---

## 🚀 Summary

These commands cover basic file navigation, filtering, and searching in PowerShell for beginners.

```.
```

