## Important Commands - Linux 

## File & Directory Commands

| Command          | What it does                         |
| ---------------- | ------------------------------------ |
| `pwd`            | Show current directory               |
| `ls`             | List files/folders                   |
| `ls -la`         | Detailed list including hidden files |
| `cd folder`      | Change directory                     |
| `mkdir name`     | Create directory                     |
| `rm file`        | Delete file                          |
| `rm -r folder`   | Delete folder recursively            |
| `cp source dest` | Copy files                           |
| `mv old new`     | Move or rename files                 |
| `touch file.txt` | Create empty file                    |
| `cat file.txt`   | View file contents                   |
| `nano file.txt`  | Edit file in Nano editor             |
| `vim file.txt`   | Edit file in Vim                     |

---

## File Search & Text Processing

| Command                 | What it does                    |
| ----------------------- | ------------------------------- |
| `find /path -name file` | Find files                      |
| `grep "text" file`      | Search text in file             |
| `grep -r "text" .`      | Recursive search                |
| `wc -l file`            | Count lines                     |
| `sort file`             | Sort lines                      |
| `uniq file`             | Remove duplicate adjacent lines |
| `head file`             | Show first 10 lines             |
| `tail file`             | Show last 10 lines              |
| `tail -f log.txt`       | Live log monitoring             |

---

## Permissions & Ownership

| Command                | What it does         |
| ---------------------- | -------------------- |
| `chmod +x file`        | Make executable      |
| `chmod 755 file`       | Change permissions   |
| `chown user:file file` | Change ownership     |
| `sudo command`         | Run as administrator |

---

## System Information

| Command         | What it does          |
| --------------- | --------------------- |
| `top`           | Live system processes |
| `htop`          | Better process viewer |
| `df -h`         | Disk usage            |
| `du -sh folder` | Folder size           |
| `free -h`       | RAM usage             |
| `uname -a`      | System info           |
| `uptime`        | System uptime         |
| `whoami`        | Current user          |

---

## Process Management

| Command       | What it does           |
| ------------- | ---------------------- |
| `ps aux`      | Show running processes |
| `kill PID`    | Kill process           |
| `kill -9 PID` | Force kill             |
| `jobs`        | Background jobs        |
| `bg`          | Resume in background   |
| `fg`          | Bring to foreground    |

---

## Networking

| Command                    | What it does        |
| -------------------------- | ------------------- |
| `ping google.com`          | Test connectivity   |
| `curl URL`                 | Fetch URL content   |
| `wget URL`                 | Download files      |
| `ssh user@host`            | Remote login        |
| `scp file user@host:/path` | Secure file copy    |
| `ip a`                     | Show IP addresses   |
| `netstat -tulnp`           | Open ports/services |

---

## Package Management

### Debian/Ubuntu

```bash
sudo apt update
sudo apt upgrade
sudo apt install package
```

### RHEL/CentOS/Fedora

```bash
sudo dnf install package
```

or

```bash
sudo yum install package
```

---

## Compression

| Command                        | What it does |
| ------------------------------ | ------------ |
| `tar -czvf file.tar.gz folder` | Compress     |
| `tar -xzvf file.tar.gz`        | Extract      |
| `zip -r file.zip folder`       | ZIP compress |
| `unzip file.zip`               | Extract ZIP  |

---

## Useful Shortcuts

| Shortcut   | Action          |
| ---------- | --------------- |
| `Ctrl + C` | Stop process    |
| `Ctrl + Z` | Suspend process |
| `Ctrl + D` | Logout/EOF      |
| `Tab`      | Auto-complete   |
| `history`  | Command history |
| `clear`    | Clear terminal  |

---

## Beginner “Must Know” Commands

```bash
ls
cd
pwd
cp
mv
rm
mkdir
touch
cat
grep
find
chmod
sudo
top
ssh
curl
```
