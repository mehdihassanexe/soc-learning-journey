# Linux File Permissions

**Room:** Linux Fundamentals (Permissions section)  
**Path:** Linux Fundamentals  
**Date:** 13 April 2026  
**Difficulty:** Medium

## What I Learned

Linux uses a permission system to control who can access files and directories.  
Every file and directory has permissions for three types of users:

- **Owner** (the user who owns the file)
- **Group** (users who belong to the same group)
- **Others** (everyone else on the system)

There are three basic permissions:
- **Read (r)** → View the content
- **Write (w)** → Modify or delete
- **Execute (x)** → Run the file (for scripts or directories to enter)

## Understanding Permission String

Example: `-rwxr-xr--`

Breakdown:
- First character: `-` = regular file, `d` = directory
- Positions 2-4: Owner permissions (`rwx`)
- Positions 5-7: Group permissions (`r-x`)
- Positions 8-10: Others permissions (`r--`)

## Numeric (Octal) Method

Permissions can also be represented using numbers:

| Permission | Value | Meaning                     |
|------------|-------|-----------------------------|
| rwx        | 7     | Read + Write + Execute      |
| rw-        | 6     | Read + Write                |
| r-x        | 5     | Read + Execute              |
| r--        | 4     | Read only                   |
| ---        | 0     | No permission               |

Common examples:
- `777` → Everyone can read, write, and execute (very insecure)
- `755` → Owner has full access, others can read and execute
- `644` → Owner can read and write, others can only read

## chmod Command

Changing permissions using `chmod`:

- Symbolic method:
  - `chmod u+x file.txt` → Add execute permission for owner
  - `chmod go-w file.txt` → Remove write permission from group and others

- Numeric method:
  - `chmod 755 file.sh` → Owner full rights, others read+execute
  - `chmod 600 private.txt` → Only owner can read and write
    
 
## Permission Effects

| Permission | Effect on File                          | Effect on Directory                          |
|------------|-----------------------------------------|----------------------------------------------|
| **r (Read)**   | Allows viewing or copying the file content | Allows listing the contents of the directory |
| **w (Write)**  | Allows modifying, deleting, or renaming the file | Allows creating, deleting, or renaming items inside the directory (requires execute permission) |
| **x (Execute)**| Allows running the file as a script or program | Allows entering (cd) into the directory |


## Memory Hook

**"rwx = 4-2-1"**  
Read = 4, Write = 2, Execute = 1 → Add them up like a combination lock.

Owner → Group → Others

## Why It Matters for SOC / Blue Team

- Incorrect file permissions are a very common security weakness
- Attackers often look for files with **777** or **666** permissions (world-writable)
- Understanding permissions is important during incident response and system hardening
- Helps in detecting privilege escalation attempts

**Status:** Completed ✅
