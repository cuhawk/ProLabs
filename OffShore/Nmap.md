Nmap scan report for 10.10.110.123
Host is up (0.021s latency).

PORT     STATE SERVICE  VERSION
22/tcp   open  ssh      OpenSSH 7.2p2 Ubuntu 4ubuntu2.10 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 edda93ee2e2b7a024d973d1bf240baf6 (RSA)
|   256 7edefa0c9d4c6c017c0a0cf1744df35f (ECDSA)
|_  256 15abfcb8a2faf157d73fbcabadd0cc99 (ED25519)
80/tcp   open  http     Apache httpd 2.4.18 ((Ubuntu))
|_http-server-header: Apache/2.4.18 (Ubuntu)
|_http-title: ACME Bank
8089/tcp open  ssl/http Splunkd httpd (free license; remote login disabled)
| http-auth: 
| HTTP/1.1 401 Unauthorized\x0D
|_  Server returned status 401 but no WWW-Authenticate header.
|_http-server-header: Splunkd
| ssl-cert: Subject: commonName=SplunkServerDefaultCert/organizationName=SplunkUser
| Not valid before: 2018-02-02T20:26:16
|_Not valid after:  2021-02-01T20:26:16
|_http-title: Site doesn't have a title (text/xml; charset=UTF-8).
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
___
Nmap scan report for 10.10.110.124
Host is up (0.023s latency).

PORT   STATE SERVICE VERSION
80/tcp open  http    Microsoft IIS httpd 10.0
| http-methods: 
|_  Potentially risky methods: TRACE
|_http-title: Offshore Dev
|_http-server-header: Microsoft-IIS/10.0
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows
___
