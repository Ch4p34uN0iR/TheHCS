# Metasploit Framework
## TheHCS / @NitescuLucian / http://www.metasploit.com/

Metasploit = World's most used penetration testing software. Metasploit Framework, a tool for developing and executing exploit code against a remote target machine.

The basic steps for exploiting a system using the Framework include:
* Choosing and configuring an exploit (code that enters a target system by taking advantage of one of its bugs; about 900 different exploits for Windows, Unix/Linux and Mac OS X systems are included);
* Optionally checking whether the intended target system is susceptible to the chosen exploit;
* Choosing and configuring a payload (code that will be executed on the target system upon successful entry; for instance, a remote shell or a VNC server);
* Choosing the encoding technique so that the intrusion-prevention system (IPS) ignores the encoded payload;
* Executing the exploit.
* This modular approach – allowing the combination of any exploit with any payload – is the major advantage of the Framework. It facilitates the tasks of attackers, exploit writers and payload writers.
Metasploit runs on Unix (including Linux and Mac OS X) and on Windows. The Metasploit Framework can be extended to use add-ons in multiple languages.

Exploits:

* Firefox is a collection of (mostly) remote code execution for this browser.
* Android and Apple's iOs are dedicated to mobile phone.
* Linux, Windows, BDSi, Irix, Solaris, … are targeting specific operating systems
* Multi for exploits that aren't tied to a specific platform

Payloads:

* Command shell enables users to run collection scripts or run arbitrary commands against the host.
* Meterpreter enables users to control the screen of a device using VNC and to browse, upload and download files.
* Dynamic payloads enables users to evade anti-virus defenses by generating unique payloads.

### Source:
* https://pentestbox.org/
* https://en.wikipedia.org/wiki/Metasploit_Project
