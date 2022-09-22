<p align="center">
	<img src="logo.png" alt="1337"/><br>
</p>

This repository is an overview of what you need to learn in penetration testing and a collection of the necessary tools you can use during your pentesting, and it is also a collection of resources and references to practice offensive security. You can always comeback here, to check if you forgot any step. This will be mainly focused only on Linux machines.

## Table of contents
- [Introduction](#introduction)
  - [What you need to know](#what-you-need-to-know)
  - [Where to practice ?](#where-to-practice-)
    - [Youtubers](#youtubers)
    - [Platforms](#platforms)
- [Before Hacking](#before-hacking)
  - [Languages](#languages)
      - [Languages you must know](#languages-you-must-know)
      - [Languages that definetly can help you out](#languages-that-definetly-can-help-you-out)
- [Steps of Pen-Testing](#steps-of-pen-testing)
- [Enumeration](#enumeration)
  - [NMAP.](#nmap)
    - [Nmap Different Commands](#nmap-different-commands)
  - [Sub Domains](#sub-domains)
  - [URL response](#url-response)
  - [Fuzzing](#fuzzing)
  - [DNS](#dns)
  - [Logs](#logs)
- [Privilege Escalation](#privilege-escalation)
  - [System Information](#system-information)
    - [OS Infos](#os-infos)
    - [Kernel Version](#kernel-version)
    - [Sudo Version](#sudo-version)
  - [Processors](#processors)
  - [Cronjobs](#cronjobs)
- [Tools](#tools)
      - [:male_detective: Information Gathering](#male_detective-information-gathering)
      - [:lock: Password Attacks](#lock-password-attacks)
          - [:memo: Wordlists](#memo-wordlists)
      - [:globe_with_meridians: Wireless Testing](#globe_with_meridians-wireless-testing)
      - [:wrench: Exploitation Tools](#wrench-exploitation-tools)
      - [:busts_in_silhouette: Sniffing & Spoofing](#busts_in_silhouette-sniffing--spoofing)
      - [:rocket: Web Hacking](#rocket-web-hacking)
      - [:tada: Post Exploitation](#tada-post-exploitation)
      - [:package: Frameworks](#package-frameworks)
- [Additional resources](#additional-resources)
- [Conclusion.](#conclusion)



# Introduction

The goal of this repository is to help out beginners-medium hackers. Practicing is the only way to improve in this domain, and there are plenty of websites where you can learn, and hack at the same time. But before that, let's talk a bit about what you will find in the repository.

## What you need to know
To become a great pentester you have to be patient. Learning and practicing are definetly your way into this domain. But it will take some time.
Here's a simple list of things you should and shouldn't do in order to imporve :

-	Don't be a script kiddie, not having any idea on what you're doing means you're a script kiddie.
-	You have to master at least one programming language. And if you still haven't learn a single programming language. I would advise you to start with Python.
-	Don't just use tools without knowing how they work. Here's a [list of tools](#tools) you will need.
-	You're not ready for real targets, just focus on [practicing and learning](#where-to-practice) and you will get there. Hopefully in a lawful way.
-	Learning doesn't only rely on videos on youtube, reading could be a great way as well. From [books](https://www.softwaretestinghelp.com/cyber-security-books/) to [manuals]([#books](https://www.naruc.org/cpi-1/critical-infrastructure-cybersecurity-and-resilience/cybersecurity/cybersecurity-manual/)) and [articles](https://github.com/reddelexc/hackerone-reports).
-	Assembly language is far important than you think, specially if you're into Reverse engineeering or PWN. It would be easier to learn it if you master C language before.
-	You have to know how computers and operating system works. Do you know what a kernel is ? If not you should do some googling.
-	Twitter, as dumb as this idea looks, but i'd really recommend you to have a twitter account, and follow [the community](https://github.com/j4k0m/AwesomeMoroccanHackers) related and be part of them. Staying up to date with the world is not such a bad idea after all.
-	Last but not least, don't learn hacking for wrong reasons. Don't waste your time if your goal is to hack your girl(boy)friends Facebook account. Set a goal, no matter how big it looks like, and chase it. [Dreams without goals are the ultimate fuel of disappointment](https://www.youtube.com/watch?v=TssZmJaoZs4&t=180s).

## Where to practice ?
Here you will find multiple resources to learn and practice hacking.

### Youtubers
Here's a list of one the best youtubers I personally follow.
| Name      	| Description																 			     | Link  |
| :-----------: |:------------------------------------------------------------------------------------------:| :----:|
| IPPSEC  | Does retired machines from HackTheBox, great way to learn what to do before every machine.                  | [link](https://www.youtube.com/c/ippsec) |
| Liveoverflow        | One of the best channels on youtube to learn reverse engineering and PWN. |   [Link](https://www.youtube.com/c/LiveOverflow) |
| John Hammond  | Does different kind of CTFs, you can learn how to use lot of tools, and techniques.        |    [Link](https://www.youtube.com/c/JohnHammond010) |
| David Bombal  | Great channel to imporve professionally in hacking if you are looking for jobs.			 | [Link](https://www.youtube.com/c/DavidBombal) |
| NetworkChuck  | If you are looking where to learn very basic stuff with a fun way (specially networking), this guy is yours.		 | [Link](https://www.youtube.com/c/NetworkChuck) |
| The Cyber Mentor	| Our cyber security mentor... This channel contains real world pentesting examples and courses, this guy will definitely be your mentor aswell. | [link](https://www.youtube.com/c/TheCyberMentor/) |
| HackerSploit  | This one explains tools, and does HackTheBox retired machines. And also does real life scenarios hacking. | [Link](https://www.youtube.com/c/HackerSploit) |

### Platforms
Here's where you can learn and practice at the same time.
| Name		    | Description																				 | Link  |
| :-----------: |:------------------------------------------------------------------------------------------:| :----:|
| HackTheBox	| Perhaps the greatest platform with the hardest possible challenge. specialise in Boxes (don't start here)	 | [HackTheBox](https://www.hackthebox.com) |
| TryHackMe		| This one is similar to HackTheBox, difference is that is has easier challenges than HTB	 | [TryHackMe](https://tryhackme.com) |
| PwnTillDawn	| Although the name would give you PWN vibes, it has a big number of boxes ready to be PWNed | [PwnTillDawn](https://online.pwntilldawn.com/) |
| CyberTalents 	| A good platform for beginners to start their journey into hacking. It has only CTFs though | [CyberTalents](https://cybertalents.com) |
| Pwnable		| Fun platform to learn PWN from the very basics. You will need to learn C language before	 | [Pwnable](https://pwnable.kr/) |
| HackThisSite	| Free platform for hackers to test and expand their knowledge with CTFs, challenges and many more | [HackThisSite](https://www.hackthissite.org/) |
| Hacker101		| Free class for web security. Whether you're a programmer with an interest in bug bounties or a seasoned security professional | [Hacker101](https://www.hacker101.com/) |
| PicoCTF		| Free computer security education program, with original created challenges to practice your skills in different domains. | [PicoCTF](https://picoctf.org/) |

Go ahead a knock yourself out.

# Before Hacking
There are certain things you need to learn before even diving into hacking. Here's a list you should definetly check out.

## Languages
Many might think that programming is not really necessary in hacking, [they're not just wrong they're stupid](https://www.youtube.com/watch?v=40Pvi1XVm_s).
But you need to know that not all programming languages serve the same purpose. There are different types, you should learn at least one language in each category. Let's go ahead and check them out.

#### Languages you must know
These are the languages that will on a daily basis in your hacking journey.

- **C / Assembly**	: Low level language, for binary exploitation.
- **Bash**		: Linux scripting language.
- **Powershell**	: Windows scripting language.
- **Python**		: Easy to learn language, that can help you automate lot of work you do frequently.
- **PHP**		: You cannot do web pentesting or bug bounty without knowing PHP.
- **Javascript**	: Learning Javascript is as important as learning PHP, specially if you are into web app security.

#### Languages that definetly can help you out
- **C++**
- **Ruby**
- **Go**
- **Java**

# Steps of Pen-Testing
In this section, We'll give you a certain steps you should always follow when you're pentesting.

<p align="center">
	<img src="https://www.tutorialspoint.com/penetration_testing/images/penetration_testing_method.jpg" alt="Pentesting" /><br>
</p>

[Learn more](https://www.tutorialspoint.com/penetration_testing/index.htm)

# Enumeration
Now since we're finished with the introduction, let's go ahead and hack a box for the sake of an example.
The Box I chose, is [Boot2Root](https://github.com/mza7a/Boot2Root), a project in 42 Cursus.

## NMAP.
The first step you should think of, is trying to identify what exactly you're attacking (hopefully in a lawful way). You need to gather maximum of informations from this target. A great way to do so, is to use a tool called [NMAP](https://linux.die.net/man/1/nmap). It's used to to scan ip addresses, it can also be used to identify ip addresses connected to your network.
Since we do not know the ip address of our box, we have to scan our network in order to identify its ip address.

Depending on what's your network class, you can use the following command in order to scan a certain subnet.

```bash
$> nmap 10.12.100.x/24
```
You will get an output similar to this :
<p align="center">
	<img src="https://i.imgur.com/OGMJrEf.png" alt="nmap result"/><br>
</p>
And as you can see we have the ip address of the machine.
But you'll ask what else we can do with nmap. Great question, can't answer it all. You have to discover more yourself. But let me show you some couple of commands you can use in order to do stuff.

### Nmap Different Commands
In order to use the following commands, you have to specify `-A` tag on your scan. It for aggressive scanning.
```bash
$> nmap -A 10.12.11.100
```

Using nmap, you can detect what Operatin System the target uses. Note that this is not always accurate, and also you will need root privelege. Here's an example :
```bash
$> sudo nmap -o 10.12.11.100
```

You can also detect what services are running on that target, the version of those services as well. Note that `-sV` is for the version scanning.
```bash
$> nmap -sV 10.12.11.100
```

How about running a scan on all the ports from in a total of 65,535 ports.
```bash
$> nmap -p- 10.12.11.100
```

You want only one port ?
```bash
$> nmap -p 80 10.22.11.100
```

How about multiple ports ?
```bash
$> nmap -p 80,443 10.22.11.100
```

A range of ports ?
```bash
$> nmap -p 80-8080 10.22.11.100
```

There is also timing templates, if you want your scan to take more or less time.
```bash
$> nmap -T[ID] 10.22.11.100
```

Sometimes you will counter targets that blocks your pings. Use the `-Pn` tag to skip the host discovery. This treats your target as an online target.
```bash
$> nmap -Pn 10.22.11.100
```

If you want to save the results of your scan you can do it like this :
```bash
$> nmap 10.22.11.100 -oA output.name
```

Let's go ahead and gather all the tags, under one powerful command, you have to know that a command like this would take ~20-30 minutes :
```bash
$> sudo nmap -A -O -Pn -p- -T4 -sV 10.22.11.100
```

There are a lot more commands than this, you should visit the [nmap man page](https://linux.die.net/man/1/nmap) or their [Docs](https://nmap.org/docs.html) to learn even more about this tool.


There are lot of other [tools](#tools) that you can use in order to dir bust, and each tools gives you different options.

## Sub Domains
Let's say you scanned a target and you found a web application, this web application can contains a multiple subdomains that you should check.

<p align="center">
	<img src="https://blog.hubspot.com/hs-fs/hubfs/Google%20Drive%20Integration/Whats%20a%20Subdomain%20%26%20How%20Is%20It%20Used%3F-3.jpeg?width=1300&name=Whats%20a%20Subdomain%20%26%20How%20Is%20It%20Used%3F-3.jpeg" alt="subdomains" /><br>
</p>

You might ask what a [subdomain](https://blog.hubspot.com/website/what-is-a-subdomain) is. It's simply a good way to seperate the content of you website. It's piece of additional information added to the beginning of a website’s domain name. It allows websites to separate and organize content for a specific function — such as a blog or an online store — from the rest of your website.

Like sub-directories, you can also search for sub-domains , using a [wordlist](#wordlists) and a tool. In this case we'll be using as an example [gobuster](https://github.com/OJ/gobuster)

Using the following command :
```bash
$> gobuster dns -d google.com  -w /path/to/wordlist.txt
-d : To specify the domain name
-w : To specify a wordlist
```

Thus you will get something like this(don't take this example seriously, it's not true... or maybe ?).
```
www.google.com
blog.google.com
store.google.com
etc...
```

This can help you find more information about a certain website that you didn't know. Maybe even find login pannels or so.

## URL response
After generating a list of subdomain and hosts, it's time to check those who work. Doing it manualy will take a long time if a long list was generated, so here's a tools [httpx](https://github.com/projectdiscovery/httpx) that make that task easy for us.
Using the following command : 
```bash
$> cat hosts.txt | httpx
```

[httpx](https://github.com/projectdiscovery/httpx) have more other intersting functionality, check the repo for more info.


## Fuzzing
You find a web app and its subdomains too, so what can you do with it.
For instance you can try and find directories or files. There are lot of [tools](#tools) you can use to do that. But for now let's use [dirb](https://www.kali.org/tools/dirb/).

You'll need wordlist, in order to test on multiple directories or files. Check [wordlists](#wordlists) for more infos.
This is an example on how to use `dirb` command.
```bash
$> dirb http://ip_add/ /path/to/wordlist
```

## DNS
A good thing to do is to pay attention to the request you make on a website. Some websites can show you different outputs depending on what domain name you requested. Specially when you're playing challenges on websites like [HackTheBox](hackthebox.com) or [TryHackMe](tryhackme.com), always change your host file to whatever you find while scanning or while enumerating in general.

```bash
$> nano /etc/hosts
10.1.1.1	1337.htb #example
```

## Logs
Logs are really important when it comes to tracing one's moves. You can even find credentials on them. We will talk more about it in the [Privilege Escalation part](#privilege-escalation)

# Privilege Escalation
Using [HackTricks](https://book.hacktricks.xyz/linux-unix/privilege-escalation), we can use multiple commands to monitor a system and thus finding an exploit we can use to privesc the system.

## System Information

### OS Infos
```
uname -a
cat /etc/os-release
cat /proc/version
```

### Kernel Version
```
uname -r
```

### Sudo Version
```
sudo -v (might not work sometimes if you don't have the password of the user)
```

## Processors
```
ps aux
ps -ef
top -n 1
```

## Cronjobs
```
crontab -l
ls -al /etc/cron* /etc/at*
cat /etc/cron* /etc/at* /etc/anacrontab /var/spool/cron/crontabs/root 2>/dev/null | grep -v "^#"
```

# Tools

#### :male_detective: Information Gathering

Information Gathering tools allows you to collect host metadata about services and users. Check informations about a domain, IP address, phone number or an email address.

| Tool        | Language           | Support  | Description    |
| ----------- |-------------------------|----------|----------------|
| [theHarvester](https://github.com/laramies/theHarvester)      | **Python** | `Linux/Windows/macOS` | E-mails, subdomains and names Harvester. |
| [CTFR](https://github.com/UnaPibaGeek/ctfr)      | **Python** | `Linux/Windows/macOS` | Abusing Certificate Transparency logs for getting HTTPS websites subdomains. |
| [Sn1per](https://github.com/1N3/Sn1per)      | **bash** | `Linux/macOS` | Automated Pentest Recon Scanner. |
| [RED Hawk](https://github.com/Tuhinshubhra/RED_HAWK)      | **PHP** | `Linux/Windows/macOS` | All in one tool for Information Gathering, Vulnerability Scanning and Crawling. A must have tool for all penetration testers. |
| [Infoga](https://github.com/m4ll0k/Infoga)      | **Python** | `Linux/Windows/macOS` | Email Information Gathering. |
| [KnockMail](https://github.com/4w4k3/KnockMail)      | **Python** | `Linux/Windows/macOS` | Check if email address exists. |
| [a2sv](https://github.com/hahwul/a2sv)      | **Python** | `Linux/Windows/macOS` | Auto Scanning to SSL Vulnerability. |
| [Wfuzz](https://github.com/xmendez/wfuzz)      | **Python** | `Linux/Windows/macOS` | Web application fuzzer. |
| [Nmap](https://github.com/nmap/nmap)      | **C/C++** | `Linux/Windows/macOS` | A very common tool. Network host, vuln and port detector. |
| [PhoneInfoga](https://github.com/sundowndev/PhoneInfoga)      | **Go** | `Linux/macOS` | An OSINT framework for phone numbers. |

#### :lock: Password Attacks

Crack passwords and create wordlists.

| Tool        | Language           | Support  | Description    |
| ----------- |-------------------------|----------|----------------|
| [John the Ripper](https://github.com/magnumripper/JohnTheRipper)      | **C** | `Linux/Windows/macOS` | John the Ripper is a fast password cracker. |
| [hashcat](https://github.com/hashcat/hashcat)      | **C** | `Linux/Windows/macOS` | World's fastest and most advanced password recovery utility. |
| [Hydra](https://github.com/vanhauser-thc/thc-hydra)      | **C** | `Linux/Windows/macOS` | Parallelized login cracker which supports numerous protocols to attack. |
| [ophcrack](https://gitlab.com/objectifsecurite/ophcrack)      | **C++** | `Linux/Windows/macOS` | Windows password cracker based on rainbow tables. |
| [Ncrack](https://github.com/nmap/ncrack)      | **C** | `Linux/Windows/macOS` | High-speed network authentication cracking tool. |
| [WGen](https://github.com/agusmakmun/Python-Wordlist-Generator)      | **Python** | `Linux/Windows/macOS` | Create awesome wordlists with Python. |
| [SSH Auditor](https://github.com/ncsa/ssh-auditor)      | **Go** | `Linux/macOS` | The best way to scan for weak ssh passwords on your network. |

###### :memo: Wordlists

| Tool        | Description    |
| ----------- |----------------|
| [Probable Wordlist](https://github.com/berzerk0/Probable-Wordlists)      | Wordlists sorted by probability originally created for password generation and testing. |
| [SecLists](https://github.com/danielmiessler/SecLists)      | A collection of multiple types of lists used during security assessments, collected in one place. List types include usernames, passwords, URLs, sensitive data patterns, fuzzing payloads, web shells, and many more. |

#### :globe_with_meridians: Wireless Testing

Used for intrusion detection and wifi attacks.

| Tool        | Language           | Support  | Description    |
| ----------- |-------------------------|----------|----------------|
| [Aircrack](https://github.com/aircrack-ng/aircrack-ng)      | **C** | `Linux/Windows/macOS` | WiFi security auditing tools suite. |
| [bettercap](https://github.com/bettercap/bettercap)      | **Go** | `Linux/Windows/macOS/Android` | bettercap is the Swiss army knife for network attacks and monitoring. |
| [WiFi Pumpkin](https://github.com/P0cL4bs/WiFi-Pumpkin)      | **Python** | `Linux/Windows/macOS/Android` | Framework for Rogue Wi-Fi Access Point Attack. |
| [Airgeddon](https://github.com/v1s1t0r1sh3r3/airgeddon)      | **Shell** | `Linux/Windows/macOS` | This is a multi-use bash script for Linux systems to audit wireless networks. |
| [Airbash](https://github.com/tehw0lf/airbash)      | **C** | `Linux/Windows/macOS` | A POSIX-compliant, fully automated WPA PSK handshake capture script aimed at penetration testing. |

#### :wrench: Exploitation Tools

Acesss systems and data with service-oriented exploits.

| Tool                                                    | Language   | Support               | Description                                                  |
| ------------------------------------------------------- | ---------- | --------------------- | ------------------------------------------------------------ |
| [SQLmap](https://github.com/sqlmapproject/sqlmap)       | **Python** | `Linux/Windows/macOS` | Automatic SQL injection and database takeover tool.          |
| [XSStrike](https://github.com/UltimateHackers/XSStrike) | **Python** | `Linux/Windows/macOS` | Advanced XSS detection and exploitation suite.               |
| [Commix](https://github.com/commixproject/commix)       | **Python** | `Linux/Windows/macOS` | Automated All-in-One OS command injection and exploitation tool.￼ |
| [Nuclei](https://github.com/projectdiscovery/nuclei)    | **Go**     | `Linux/Windows/macOS` | Fast and customisable vulnerability scanner based on simple YAML based DSL. |

#### :busts_in_silhouette: Sniffing & Spoofing

Listen to network traffic or fake a network entity.

| Tool        | Language           | Support  | Description    |
| ----------- |-------------------------|----------|----------------|
| [Wireshark](https://www.wireshark.org)      | **C/C++** | `Linux/Windows/macOS` | Wireshark is a network protocol analyzer. |
| [WiFi Pumpkin](https://github.com/P0cL4bs/WiFi-Pumpkin)      | **Python** | `Linux/Windows/macOS/Android` | Framework for Rogue Wi-Fi Access Point Attack. |
| [Zarp](https://github.com/hatRiot/zarp)      | **Python** | `Linux/Windows/macOS` | A free network attack framework. |

#### :rocket: Web Hacking

Exploit popular CMSs that are hosted online.

| Tool        | Language           | Support  | Description    |
| ----------- |-------------------------|----------|----------------|
| [WPScan](https://github.com/wpscanteam/wpscan)      | **Ruby** | `Linux/Windows/macOS` | WPScan is a black box WordPress vulnerability scanner. |
| [Droopescan](https://github.com/droope/droopescan)      | **Python** | `Linux/Windows/macOS` | A plugin-based scanner to identify issues with several CMSs, mainly Drupal & Silverstripe. |
| [Joomscan](https://github.com/rezasp/joomscan)      | **Perl** | `Linux/Windows/macOS` | Joomla Vulnerability Scanner. |
| [Drupwn](https://github.com/immunIT/drupwn)      | **Python** | `Linux/Windows/macOS` | Drupal Security Scanner to perform enumerations on Drupal-based web applications. |
| [CMSeek](https://github.com/Tuhinshubhra/CMSeek)      | **Python** | `Linux/Windows/macOS` | CMS Detection and Exploitation suite - Scan WordPress, Joomla, Drupal and 130 other CMSs. |

#### :tada: Post Exploitation

Exploits for after you have already gained access.

| Tool        | Language           | Support  | Description    |
| ----------- |-------------------------|----------|----------------|
| [TheFatRat](https://github.com/Screetsec/TheFatRat)      | **C** | `Linux/Windows/macOS` | Easy tool to generate backdoor and easy tool to post exploitation attack like browser attack, dll. |

#### :package: Frameworks

Frameworks are packs of pen testing tools with custom shell navigation and documentation.

| Tool        | Language           | Support  | Description    |
| ----------- |-------------------------|----------|----------------|
| [Operative Framework](https://github.com/graniet/operative-framework)      | **Python** | `Linux/Windows/macOS` | Framework based on fingerprint action, this tool is used to get information on a website or a enterprise target with multiple modules. |
| [Metasploit](https://github.com/rapid7/metasploit-framework)      | **Ruby** | `Linux/Windows/macOS` | A penetration testing framework for ethical hackers. |
| [cSploit](https://github.com/cSploit/android)      | **Java** | `Android` | The most complete and advanced IT security professional toolkit on Android. |
| [radare2](https://github.com/radare/radare2)      | **C** | `Linux/Windows/macOS/Android` | Unix-like reverse engineering framework and commandline tools. |
| [Wifiphisher](https://github.com/wifiphisher/wifiphisher)      | **Python** | `Linux` | The Rogue Access Point Framework. |
| [Beef](https://github.com/beefproject/beef)      | **Javascript** | `Linux/Windows/macOS` | The Browser Exploitation Framework. It is a penetration testing tool that focuses on the web browser. |
| [Mobile Security Framework (MobSF)](https://github.com/MobSF/Mobile-Security-Framework-MobSF)      | **Python** | `Linux/Windows/macOS` | Mobile Security Framework (MobSF) is an automated, all-in-one mobile application (Android/iOS/Windows) pen-testing, malware analysis and security assessment framework capable of performing static and dynamic analysis. |
| [Burp Suite](https://portswigger.net/burp)      | **Java** | `Linux/Windows/macOS` | Burp Suite is a leading range of cybersecurity tools, brought to you by PortSwigger. **This tool is not free and open source** |

# Additional resources

- [The Life of a Security Researcher](https://www.alienvault.com/blogs/security-essentials/the-life-of-a-security-researcher)
- [Awesome-Hacking Lists](https://github.com/Hack-with-Github/Awesome-Hacking/blob/master/README.md)
- [Security Mindmap](https://github.com/dsopas/assessment-mindset)
- [Exploit Database](http://www.exploit-db.com/)
- [Hackavision](http://www.hackavision.com/)
- [Hackmethod](https://www.hackmethod.com/)
- [Packet Storm Security](http://packetstormsecurity.org/)
- [SecLists](http://seclists.org/)
- [SecTools](http://sectools.org/)
- [Smash the Stack](http://smashthestack.org/)
- [Don't use VPN services](https://gist.github.com/joepie91/5a9909939e6ce7d09e29)
- [How to Avoid Becoming a Script Kiddie](https://www.wikihow.com/Avoid-Becoming-a-Script-Kiddie)
- [2017 Top 10 Application Security Risks](https://www.owasp.org/index.php/Top_10-2017_Top_10)
- [Starting in cybersecurity ?](https://blog.0day.rocks/starting-in-cybersecurity-5b02d827fb54)

I would highly advise you guys to go and checkout [sundowndev](https://github.com/sundowndev/hacker-roadmap).

# Conclusion.
The idea behind this repository is to help promoting cyber and information security across our club, and teach the various tools used in offensive cyber security.
