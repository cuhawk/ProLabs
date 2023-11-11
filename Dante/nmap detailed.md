Nmap scan report for 172.16.1.10
Host is up (0.049s latency).

PORT    STATE SERVICE     VERSION
22/tcp  open  ssh         OpenSSH 8.2p1 Ubuntu 4ubuntu0.5 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   3072 5a9c1ba5c17f2d4f4be8cc7be447bca9 (RSA)
|   256 fdd63a3fa804564ce276db85910c5e42 (ECDSA)
|_  256 e2d5177c5875265be11b98393b2c6cfc (ED25519)
80/tcp  open  http        Apache httpd 2.4.41 ((Ubuntu))
|_http-server-header: Apache/2.4.41 (Ubuntu)
|_http-title: Dante Hosting
139/tcp open  netbios-ssn Samba smbd 4.6.2
445/tcp open  netbios-ssn Samba smbd 4.6.2
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

---
Nmap scan report for 172.16.1.12                                                                                                                                                                               
Host is up (0.10s latency).                                                                                                                                                                                    

PORT     STATE SERVICE  VERSION                                                                                                                                                                                
21/tcp   open  ftp                                                                                                                                                                                             
| fingerprint-strings:                                                                                                                                                                                         
|   DNSVersionBindReqTCP:                                                                                                                                                                                      
|     220 ProFTPD Server (ProFTPD) [::ffff:172.16.1.12]                                                                                                                                                        
|   GenericLines:                                                                                                                                                                                              
|     220 ProFTPD Server (ProFTPD) [::ffff:172.16.1.12]                                                                                                                                                        
|     Invalid command: try being more creative                                                                                                                                                                 
|_    Invalid command: try being more creative                                                                                                                                                                 
22/tcp   open  ssh      OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)                                                                                                                           
| ssh-hostkey:                                                                                                                                                                                                 
|   2048 22cca3e87dd5656d9dea17d1d91b32cb (RSA)                                                                                                                                                                
|   256 04fbb61adb9546b72213612476801eb8 (ECDSA)                                                                                                                                                               
|_  256 aec455676ebeba6554a3c3fc0829240e (ED25519)                                                                                                                                                             
80/tcp   open  http     Apache httpd 2.4.43 ((Unix) OpenSSL/1.1.1g PHP/7.4.7 mod_perl/2.0.11 Perl/v5.30.3)                                                                                                     
|_http-server-header: Apache/2.4.43 (Unix) OpenSSL/1.1.1g PHP/7.4.7 mod_perl/2.0.11 Perl/v5.30.3                                                                                                               
| http-title: Welcome to XAMPP                                                                                                                                                                                 
|_Requested resource was http://172.16.1.12/dashboard/                                                                                                                                                         
443/tcp  open  ssl/http Apache httpd 2.4.43 ((Unix) OpenSSL/1.1.1g PHP/7.4.7 mod_perl/2.0.11 Perl/v5.30.3)                                                                                                     
|_http-server-header: Apache/2.4.43 (Unix) OpenSSL/1.1.1g PHP/7.4.7 mod_perl/2.0.11 Perl/v5.30.3                                                                                                               
| tls-alpn:                                                                                                                                                                                                    
|_  http/1.1                                       
| http-title: Welcome to XAMPP
|_Requested resource was https://172.16.1.12/dashboard/
|_ssl-date: TLS randomness does not represent time
| ssl-cert: Subject: commonName=localhost/organizationName=Apache Friends/stateOrProvinceName=Berlin/countryName=DE
| Not valid before: 2004-10-01T09:10:30
|_Not valid after:  2010-09-30T09:10:30
3306/tcp open  mysql?                              
| fingerprint-strings:                             
|   DNSStatusRequestTCP, DNSVersionBindReqTCP, GenericLines, GetRequest, HTTPOptions, Help, Kerberos, NULL, RPCCheck, RTSPRequest, SMBProgNeg, SSLSessionReq, TLSSessionReq, TerminalServerCookie, X11Probe: 
|_    Host '172.16.1.100' is not allowed to connect to this MariaDB server

---
Nmap scan report for 172.16.1.19
Host is up (0.073s latency).

PORT      STATE SERVICE VERSION
80/tcp    open  http    Apache httpd 2.4.41
|_http-server-header: Apache/2.4.41 (Ubuntu)
|_http-title: Index of /
8080/tcp  open  http    Jetty 9.4.27.v20200227
|_http-server-header: Jetty(9.4.27.v20200227)
|_http-title: Site doesn't have a title (text/html;charset=utf-8).
| http-robots.txt: 1 disallowed entry 
|_/
33060/tcp open  mysqlx?
| fingerprint-strings: 
|   NotesRPC, SSLSessionReq: 
|     Invalid message"
|_    HY000

---
Nmap scan report for 172.16.2.5
Host is up (0.61s latency).

PORT    STATE SERVICE       VERSION
53/tcp  open  domain        Simple DNS Plus
88/tcp  open  kerberos-sec  Microsoft Windows Kerberos (server time: 2023-06-24 22:03:46Z)
135/tcp open  msrpc         Microsoft Windows RPC
139/tcp open  netbios-ssn   Microsoft Windows netbios-ssn
389/tcp open  ldap          Microsoft Windows Active Directory LDAP (Domain: DANTE.ADMIN0., Site: Default-First-Site-Name)
445/tcp open  microsoft-ds?
Service Info: Host: DANTE-DC02; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb2-security-mode: 
|   311: 
|_    Message signing enabled and required
| smb2-time: 
|   date: 2023-06-24T22:03:55
|_  start_date: N/A
