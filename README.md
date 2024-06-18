# Personal Hacking Notes!

## Introduction

This repository contains my penetration testing notes, covering each phase. Whether you're a beginner or an experienced professional, you'll find valuable information to enhance your cybersecurity skills.

## Information Gathering

Information gathering describes how we obtain information about the necessary components in various ways. We search for information about the target company and the software and hardware in use to find potential security gaps that we may be able to leverage for a foothold.

### Notes
- Techniques for gathering information
- Tools commonly used
- Case studies and examples

## Vulnerability Assessment

Once we get to the Vulnerability Assessment stage, we analyze the results from our Information Gathering stage, looking for known vulnerabilities in the systems, applications, and various versions of each to discover possible attack vectors.

### Notes
- Methods for vulnerability assessment
- Manual vs automated assessment
- Tools and resources
- Examples of common vulnerabilities

## Exploitation

In the Exploitation stage, we use the results to test our attacks against the potential vectors and execute them against the target systems to gain initial access to those systems.

### Notes
- Common exploitation techniques
- Tools and frameworks
- Real-world examples and case studies

## Post-Exploitation

At this stage of the penetration test, we already have access to the exploited machine and ensure that we still have access to it even if modifications and changes are made.

### Notes
- Privilege escalation techniques
- Persistence mechanisms
- Data exfiltration strategies

## Lateral Movement

Lateral movement describes movement within the internal network of our target company to access additional hosts at the same or a higher privilege level.

### Notes
- Techniques for lateral movement
- Tools and methods
- Examples and case studies

## Proof-of-Concept

In this stage, we document, step-by-step, the steps we took to achieve network compromise or some level of access.

### Notes
- Documentation best practices
- Creating scripts for reproducibility
- Example documentation

## Post-Engagement

During post-engagement, detailed documentation is prepared for both administrators and client company management to understand the severity of the vulnerabilities found.

### Notes
- Preparing reports
- Cleanup procedures
- Deliverables and presentations

## Contributing

We welcome contributions from the community! If you'd like to contribute, please follow these guidelines:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes.
4. Push your branch and open a pull request.

## Syllabus

- [Information Gathering](/General/Information%20Gathering/informationGathering.md)
  - [Pasive](/General/Information%20Gathering/pasiveInfo.md)
  - [Active](/General/Information%20Gathering/activeInfo.md)

- [Scanning & Footprinting](/General/Scanning%20&%20Footprinting/scannFootprint.md)
  - [Mapping a Network](/General/Scanning%20&%20Footprinting/netMap.md)
  - [Port Scanning](/General/Scanning%20&%20Footprinting/portScan.md)

- [Enumeration](/General/Enumeration/enumeration.md)
  - [SMB](/General/Enumeration/smb.md)
  - [FTP](/General/Enumeration/ftp.md)
  - [SSH](/General/Enumeration/ssh.md)
  - [HTTP](/General/Enumeration/http.md)
  - [SQL](/General/Enumeration/sql.md)
  - [SMTP](/General/Enumeration/smtp.md)

- [Exploitation](/General/Exploitation/exploitation.md)

    - [Host Based Attacks](/General/Exploitation/Host%20Based%20Attacks/hostBased.md)
        - [Windows](/General/Exploitation/Host%20Based%20Attacks/windowsHost.md)
        - [Linux](/General/Exploitation/Host%20Based%20Attacks/linuxHost.md)
        - [Exploits](/General/Exploitation/Host%20Based%20Attacks/exploits.md)

    - [Network Based Attacks](/General/Exploitation/Network%20Based%20Attacks/netBased.md)
 
    - [Web](/General/Exploitation/Web/web.md)
        - [Web Enumeration](/General/Exploitation/Web/webEnumeration.md)
        - [Web Attacks](/General/Exploitation/Web/webAttacks.md)
 
    - [Metasploit](/General/Exploitation/Metasploit/metasploit.md)

    
- [Post Exploitation](/General/Post%20Exploitation/postExpl.md)

    - [Post Exp Enumeration](/General/Post%20Exploitation/Post%20Exploitation%20Enumeration/postExpEnumeration.md)

    - [File Transferring](/General/Post%20Exploitation/Transferring%20FIles/fileTrans.md)
 
    - [Shells](/General/Post%20Exploitation/Shells/shells.md)
  
    - [Privilege Escalation](/General/Post%20Exploitation/Privilege%20Escalation/privEsc.md)
        - [Windows PrivEsc](/General/Post%20Exploitation/Privilege%20Escalation/winPrivEsc.md)
        - [Linux PrivEsc](/General/Post%20Exploitation/Privilege%20Escalation/linPrivEsc.md)

    - [Credential Dumping](/General/Post%20Exploitation/Credential%20Dumping/credDump.md)
        - [Windows CredDump](/General/Post%20Exploitation/Credential%20Dumping/winCredDump.md)
        - [Linux CredDump](/General/Post%20Exploitation/Credential%20Dumping/linCredDump.md)

    - [Persistance](/General/Post%20Exploitation/Persistance/persistance.md)
        - [Windows Persistance](/General/Post%20Exploitation/Persistance/winPers.md)
        - [Linux Persistance](/General/Post%20Exploitation/Persistance/linPers.md)

    - [Clearing Tracks](/General/Post%20Exploitation/Clearing%20Tracks/clearTracks.md)

- [Social Engineering](/General/Social%20Engineering/socialEng.md)



