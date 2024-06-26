 # Personal Hacking Notes!

## Introduction

This repository contains all the notes I take during my certifications studying. I tried to cover each phase of a Penetration Test to be able to acces them easily. Whether you're a beginner or an experienced professional, you'll find valuable information to enhance your cybersecurity skills.

## Information Gathering

Information gathering describes how we obtain information about the necessary components in various ways. We search for information about the target company and the software and hardware in use to find potential security gaps that we may be able to leverage for a foothold.

- Techniques for gathering information
- Tools commonly used

## Vulnerability Assessment

Once we get to the Vulnerability Assessment stage, we analyze the results from our Information Gathering stage, looking for known vulnerabilities in the systems, applications, and various versions of each to discover possible attack vectors.

- Methods for vulnerability assessment
- Manual vs automated assessment
- Tools and resources
- Examples of common vulnerabilities

## Exploitation

In the Exploitation stage, we use the results to test our attacks against the potential vectors and execute them against the target systems to gain initial access to those systems.

- Common exploitation techniques
- Tools and frameworks

## Post-Exploitation

At this stage of the penetration test, we already have access to the exploited machine and ensure that we still have access to it even if modifications and changes are made.

- Privilege escalation techniques
- Persistence mechanisms
- Data exfiltration strategies

## Lateral Movement

Lateral movement describes movement within the internal network of our target company to access additional hosts at the same or a higher privilege level.

- Techniques for lateral movement
- Tools and methods

## Proof-of-Concept

In this stage, we document, step-by-step, the steps we took to achieve network compromise or some level of access.

- Documentation best practices
- Creating scripts for reproducibility

## Post-Engagement

During post-engagement, detailed documentation is prepared for both administrators and client company management to understand the severity of the vulnerabilities found.

- Preparing reports
- Cleanup procedures
- Deliverables and presentations

## Contributing

All contributions will be welcome! If you'd like to contribute, please follow these guidelines:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes.
4. Push your branch and open a pull request.

## Syllabus

- [Information Gathering & Vulnerability Assesment Syllabus](/General/Information%20Gathering%20&%20Vulnerability%20Assesment/Information%20Gathering%20Syllabus.md)
	
	- [Pasive Gathering](/General/Information%20Gathering%20&%20Vulnerability%20Assesment/OSINT%20-%20Passive%20Information%20Gathering.md)
	- [Active Gathering](/General/Information%20Gathering%20&%20Vulnerability%20Assesment/Active%20Information%20Gathering.md)
	- [Mapping a Network (Discovering)](/General/Information%20Gathering%20&%20Vulnerability%20Assesment/Mapping%20a%20Network.md)
	- [Port Scanning](/General/Information%20Gathering%20&%20Vulnerability%20Assesment/Port%20Scanning.md)
	-  [Bypass Secutrity Measures](/General/Information%20Gathering%20&%20Vulnerability%20Assesment/Bypass%20Security%20Measures.md)
	- [Enumeration](/General/Information%20Gathering%20&%20Vulnerability%20Assesment/enumeration.md)
		- [SMB](/General/Information%20Gathering%20&%20Vulnerability%20Assesment/Enumeration/smb.md)
		- [FTP](/General/Information%20Gathering%20&%20Vulnerability%20Assesment/Enumeration/ftp.md)
		- [SSH](/General/Information%20Gathering%20&%20Vulnerability%20Assesment/Enumeration/ssh.md)
		- [HTTP](/General/Information%20Gathering%20&%20Vulnerability%20Assesment/Enumeration/http.md)
		- [SQL](/General/Information%20Gathering%20&%20Vulnerability%20Assesment/Enumeration/sql.md)
		- [SMTP](/General/Information%20Gathering%20&%20Vulnerability%20Assesment/Enumeration/smtp.md)


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


- [Lateral Movement]()


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



