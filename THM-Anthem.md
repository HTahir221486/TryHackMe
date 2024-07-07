ist 
```console
┌──(husnain㉿husnain)-[~]
└─$ sudo nmap -sV -sC -Pn --script vuln 10.10.200.125 -vv
Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-07-07 21:25 PKT
NSE: Loaded 150 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 2) scan.
Initiating NSE at 21:25
Completed NSE at 21:25, 10.01s elapsed
NSE: Starting runlevel 2 (of 2) scan.
Initiating NSE at 21:25
Completed NSE at 21:25, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 21:25
Completed Parallel DNS resolution of 1 host. at 21:25, 0.01s elapsed
Initiating SYN Stealth Scan at 21:25
Scanning 10.10.200.125 [1000 ports]
Discovered open port 3389/tcp on 10.10.200.125
Discovered open port 80/tcp on 10.10.200.125
Completed SYN Stealth Scan at 21:25, 21.61s elapsed (1000 total ports)
Initiating Service scan at 21:25
Scanning 2 services on 10.10.200.125
Completed Service scan at 21:25, 8.57s elapsed (2 services on 1 host)
NSE: Script scanning 10.10.200.125.
NSE: Starting runlevel 1 (of 2) scan.
Initiating NSE at 21:25
NSE Timing: About 96.69% done; ETC: 21:26 (0:00:01 remaining)
NSE Timing: About 97.80% done; ETC: 21:26 (0:00:01 remaining)
NSE Timing: About 98.53% done; ETC: 21:27 (0:00:01 remaining)
NSE Timing: About 98.53% done; ETC: 21:27 (0:00:02 remaining)
NSE Timing: About 99.63% done; ETC: 21:28 (0:00:01 remaining)
NSE Timing: About 99.63% done; ETC: 21:28 (0:00:01 remaining)
NSE Timing: About 99.63% done; ETC: 21:29 (0:00:01 remaining)
NSE Timing: About 99.63% done; ETC: 21:29 (0:00:01 remaining)
NSE Timing: About 99.63% done; ETC: 21:30 (0:00:01 remaining)
NSE Timing: About 99.63% done; ETC: 21:30 (0:00:01 remaining)
NSE Timing: About 99.63% done; ETC: 21:31 (0:00:01 remaining)
NSE Timing: About 99.63% done; ETC: 21:31 (0:00:01 remaining)
NSE Timing: About 99.63% done; ETC: 21:32 (0:00:01 remaining)
NSE Timing: About 99.63% done; ETC: 21:32 (0:00:02 remaining)
NSE Timing: About 99.63% done; ETC: 21:33 (0:00:02 remaining)
NSE Timing: About 99.63% done; ETC: 21:33 (0:00:02 remaining)
NSE Timing: About 99.63% done; ETC: 21:34 (0:00:02 remaining)
NSE Timing: About 99.63% done; ETC: 21:34 (0:00:02 remaining)
NSE Timing: About 99.63% done; ETC: 21:35 (0:00:02 remaining)
NSE Timing: About 99.63% done; ETC: 21:35 (0:00:02 remaining)
NSE Timing: About 99.63% done; ETC: 21:36 (0:00:02 remaining)
NSE Timing: About 99.63% done; ETC: 21:36 (0:00:02 remaining)
NSE Timing: About 99.63% done; ETC: 21:37 (0:00:03 remaining)
NSE Timing: About 99.63% done; ETC: 21:37 (0:00:03 remaining)
NSE Timing: About 99.63% done; ETC: 21:38 (0:00:03 remaining)
NSE Timing: About 99.63% done; ETC: 21:38 (0:00:03 remaining)
NSE Timing: About 99.63% done; ETC: 21:39 (0:00:03 remaining)
NSE Timing: About 99.63% done; ETC: 21:39 (0:00:03 remaining)
NSE Timing: About 99.63% done; ETC: 21:40 (0:00:03 remaining)
Completed NSE at 21:40, 871.35s elapsed
NSE: Starting runlevel 2 (of 2) scan.
Initiating NSE at 21:40
Completed NSE at 21:40, 11.64s elapsed
Nmap scan report for 10.10.200.125
Host is up, received user-set (0.24s latency).
Scanned at 2024-07-07 21:25:25 PKT for 913s
Not shown: 998 filtered tcp ports (no-response)
PORT     STATE SERVICE       REASON          VERSION
80/tcp   open  http          syn-ack ttl 124 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-jsonp-detection: Couldn't find any JSONP endpoints.
|_http-dombased-xss: Couldn't find any DOM based XSS.
|_http-stored-xss: Couldn't find any stored XSS vulnerabilities.
|_http-wordpress-users: [Error] Wordpress installation was not found. We couldn't find wp-login.php
| http-csrf: 
| Spidering limited to: maxdepth=3; maxpagecount=20; withinhost=10.10.200.125
|   Found the following possible CSRF vulnerabilities: 
|     
|     Path: http://10.10.200.125:80/
|     Form id: 
|     Form action: /search
|     
|     Path: http://10.10.200.125:80/tags
|     Form id: 
|     Form action: /search
|     
|     Path: http://10.10.200.125:80/categories
|     Form id: 
|     Form action: /search
|     
|     Path: http://10.10.200.125:80/search
|     Form id: 
|     Form action: /search
|     
|     Path: http://10.10.200.125:80/archive/a-cheers-to-our-it-department/
|     Form id: 
|     Form action: /search
|     
|     Path: http://10.10.200.125:80/archive/we-are-hiring/
|     Form id: 
|     Form action: /search
|     
|     Path: http://10.10.200.125:80/authors/jane-doe/
|     Form id: 
|     Form action: /search
|     
|     Path: http://10.10.200.125:80/rss/%7Blink%7D
|     Form id: 
|     Form action: /search
|     
|     Path: http://10.10.200.125:80/authors/jane-doe/THM%7BL0L_WH0_D15%7D
|     Form id: 
|_    Form action: /search
|_http-litespeed-sourcecode-download: Request with null byte did not work. This web server might not be vulnerable
| http-enum: 
|   /blog/: Blog
|   /rss/: RSS or Atom feed
|   /robots.txt: Robots file
|   /categories/viewcategory.aspx: MS Sharepoint
|   /categories/allcategories.aspx: MS Sharepoint
|_  /authors/: Potentially interesting folder
3389/tcp open  ms-wbt-server syn-ack ttl 124 Microsoft Terminal Services
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 2) scan.
Initiating NSE at 21:40
Completed NSE at 21:40, 0.00s elapsed
NSE: Starting runlevel 2 (of 2) scan.
Initiating NSE at 21:40
Completed NSE at 21:40, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 923.65 seconds
           Raw packets sent: 2007 (88.308KB) | Rcvd: 11 (484B)

```
second

```console
| http-enum: 
|   /blog/: Blog
|   /rss/: RSS or Atom feed
|   /robots.txt: Robots file
|   /categories/viewcategory.aspx: MS Sharepoint
|   /categories/allcategories.aspx: MS Sharepoint
|_  /authors/: Potentially interesting folder
3389/tcp open  ms-wbt-server syn-ack ttl 124 Microsoft Terminal Services
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
```

