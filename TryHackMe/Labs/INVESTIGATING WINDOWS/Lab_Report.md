# TryHackMe - Investigating Windows

## Objective

Investigate a compromised Windows machine to identify indicators of compromise (IoCs), attacker activity, persistence mechanisms, and forensic evidence using native Windows tools.

---

## Skills Practiced

- Windows host investigation
- PowerShell enumeration
- Windows command-line administration
- Windows Event Viewer analysis
- User account enumeration
- Scheduled Task investigation
- Windows Firewall analysis
- Host file analysis
- Basic digital forensics
- Timeline analysis
- Identifying Indicators of Compromise (IoCs)
---

## Investigation Process

### 1. Identify the Operating System

**Tool Used**
- PowerShell

**Command**

```powershell
systeminfo
```

Used to determine the Windows version, build, and operating system information.

---

### 2. Investigate User Activity

**Commands**

```powershell
net user
net user <username>
```

Used to determine:

- User account information
- Last logon times
- Password information
- Group memberships

---

### 3. Identify Administrator Accounts

**Command**

```cmd
net localgroup Administrators
```

Used to enumerate all users with local administrator privileges.

---

### 4. Investigate Scheduled Tasks

**Tool**

```text
taskschd.msc
```

Reviewed scheduled tasks for persistence techniques and searched for Indicators of Compromise such as:

- Suspicious task names
- Hidden PowerShell execution
- Unusual executables
- Unexpected task actions

---

### 5. Investigate Network Activity

Observed network connections established during system startup and reviewed listening ports associated with suspicious processes.

---

### 6. Timeline Analysis

Collected timestamps from multiple artifacts to determine:

- User logon activity
- Estimated compromise time
- Privileged logon events

---

### 7. Windows Event Logs

Reviewed Security Event Logs to investigate authentication events and privilege escalation.

Techniques used included filtering Windows Event IDs to identify relevant security events.

---

### 8. Malware Investigation

Investigated temporary directories for attacker tools and suspicious executables.

Focused on:

- Temporary files
- Credential dumping tools
- Malware artifacts

---

### 9. Host File Analysis

Reviewed the Windows Hosts file for evidence of:

- DNS poisoning
- Malicious redirections
- Command and Control (C2) infrastructure

Location:

```
C:\Windows\System32\drivers\etc\hosts
```

---

### 10. Web Server Investigation

Reviewed the IIS web directory for uploaded files and suspicious extensions.

---

### 11. Firewall Investigation

Reviewed Windows Defender Firewall inbound rules to identify ports opened by the attacker.

---

## Tools Used

- PowerShell
- Command Prompt
- Event Viewer
- Task Scheduler
- Windows Defender Firewall
- Windows Explorer

---

## Key Takeaways

- Learned how to investigate a compromised Windows endpoint using built-in Windows utilities.
- Practiced identifying persistence mechanisms through Scheduled Tasks.
- Investigated Windows Event Logs for evidence of attacker activity.
- Performed basic host-based forensic analysis without relying on third-party forensic tools.
- Strengthened understanding of common Windows artifacts used during incident response.
