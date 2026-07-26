Objetives:  In part 1 of the Windows Fundamentals module, we'll start our journey learning about the Windows desktop, the NTFS file system, UAC, the Control Panel, Task Manager and more. This module is simoply a overview of the foundational aspects of Windows. 





# Notes: 
# Windows Fundamentals 1

## Overview

Windows Fundamentals 1 introduced the core components of the Windows operating system, including the NTFS file system, user accounts and permissions, User Account Control (UAC), Control Panel, Settings, and Task Manager.

---

## Key Concepts

### NTFS (New Technology File System)

- Default file system used by modern Windows operating systems.
- Journaling file system that can recover from disk errors.
- Supports:
  - Files larger than 4 GB
  - File and folder permissions
  - Compression
  - Encryption (EFS)

### NTFS Permissions

Common permissions include:

- Full Control
- Modify
- Read & Execute
- List Folder Contents
- Read
- Write

### Alternate Data Streams (ADS)

- NTFS feature allowing a file to contain multiple data streams.
- Hidden from Windows Explorer by default.
- Can be viewed using PowerShell or third-party tools.
- Has been abused by malware to hide data.

---

## Windows Directory

**Default Location**

```
C:\Windows
```

The Windows directory contains the operating system files.

Useful environment variable:

```
%windir%
```

Environment variables store important information such as system paths and temporary file locations.

---

## System32

```
C:\Windows\System32
```

One of the most important folders in Windows.

Contains:

- DLL files (shared libraries)
- EXE files (Windows utilities)
- Device drivers
- Registry-related system files

Deleting or modifying files inside System32 may render Windows unusable.

---

## User Accounts

Windows supports two main account types:

### Administrator

- Install software
- Create and remove users
- Change system settings

### Standard User

- Access personal files
- Cannot perform system-wide administrative tasks

User profiles are stored in:

```
C:\Users\<Username>
```

---

## Local Users and Groups

Launch using:

```
lusrmgr.msc
```

Administrators assign users to groups.

Users inherit the permissions of the groups they belong to.

---

## User Account Control (UAC)

Purpose:

- Reduces the risk of malware gaining administrator privileges.
- Prompts users before allowing privileged actions.

Important concepts:

- Admin users run with standard privileges until elevation is approved.
- Applications displaying the shield icon require elevated permissions.
- Child processes inherit the integrity level of the parent process.

---

## Settings vs Control Panel

### Settings

- Modern interface
- Used for common system configuration

### Control Panel

- Traditional administrative interface
- Used for advanced system configuration

---

## Task Manager

Provides information about:

- Running applications
- Background processes
- CPU usage
- Memory usage
- Startup applications

Can also be used to terminate unresponsive programs.

---

## Commands Learned

```
lusrmgr.msc
```

Opens Local Users and Groups.

---

## Key Takeaways

- Learned the structure of the Windows operating system.
- Understood how NTFS improves security and reliability.
- Learned the differences between Administrator and Standard User accounts.
- Understood how UAC protects Windows against unauthorized changes.
- Became familiar with common administrative tools such as Control Panel, Settings, Local Users and Groups, and Task Manager.
