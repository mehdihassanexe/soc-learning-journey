# 📝 Topic: Packages & Software Repositories  
**Date:** 30 April 2026  
**Room / Module:** Linux Fundamentals → Package Management  

---

## 🔑 Key Points

- Software is installed from **repositories (repos)**  
- A repo = 📦 collection of software packages  
- Managed using **APT (Advanced Package Tool)**  
- Supports **install, update, remove**  
- Can add **third-party/community repos**

---

## 📦 Core Components

- **APT** → 🛠️ Package manager (install/remove/update)  
- **Repositories** → 📚 Software sources  
- **GPG Keys** → 🔐 Verify trusted software  
- **sources.list** → 🧾 Repo registry file  

---

## ⚙️ Basic Commands

### Update repo list
```bash
sudo apt update
````

### Install software

```bash
sudo apt install <package>
```

### Remove software

```bash
sudo apt remove <package>
```

---

## ➕ Adding a Repository (Example Flow)

### 1️⃣ Add GPG Key 🔐

```bash
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
```

### 2️⃣ Create repo file 🧾

```bash
sudo nano /etc/apt/sources.list.d/sublime-text.list
```

### 3️⃣ Add repo entry

```bash
deb https://download.sublimetext.com/ apt/stable/
```

### 4️⃣ Update system 🔄

```bash
sudo apt update
```

### 5️⃣ Install package 📦

```bash
sudo apt install sublime-text
```

---

## ❌ Removing

### Remove software

```bash
sudo apt remove sublime-text
```

### Remove repository

```bash
sudo rm /etc/apt/sources.list.d/sublime-text.list
sudo apt update
```

---

## 🧠 Memory Hook

**Repo → Update → Install → Use → Remove**

---

## 🎯 Core Anchors (MOST IMPORTANT)

* **APT = HOW** → 🛠️ install/manage software
* **Repo = WHERE** → 📚 software comes from
* **GPG = TRUST** → 🔐 verifies authenticity

👉 If you remember ONLY these → you're solid

---

## ⚡ Mental Model (Easy Story)

* Add repo → 📚 “New app store added”
* Update → 🔄 “Refresh app list”
* Install → 📦 “Download & install app”
* Remove → ❌ “Uninstall app”

---

## 🛡️ Why It Matters for SOC

* Detect **malicious repositories** 🚨
* Monitor **unauthorized software installs**
* Identify **supply chain risks** 🔐
* Investigate suspicious package activity

---

## ❓ Questions / Confusions

* Difference between `apt` vs `dpkg` 🤔
* Why GPG keys are critical 🔐
* When to trust third-party repos ⚠️

---

**Status:** 🔁 Needs Review
