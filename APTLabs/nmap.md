10.10.110.0/24

---
nmap -p- --min-rate 10000 10.10.110.0/24
Starting Nmap 7.93 ( https://nmap.org ) at 2023-02-10 11:27 EST
Nmap scan report for 10.10.110.2
Host is up (0.031s latency).
All 65535 scanned ports on 10.10.110.2 are in ignored states.
Not shown: 65535 filtered tcp ports (no-response)

Nmap scan report for 10.10.110.13
Host is up (0.040s latency).
Not shown: 65533 filtered tcp ports (no-response)
PORT    STATE SERVICE
53/tcp  open  domain
443/tcp open  https

Nmap scan report for 10.10.110.21
Host is up (0.037s latency).
All 65535 scanned ports on 10.10.110.21 are in ignored states.
Not shown: 65535 filtered tcp ports (no-response)

Nmap scan report for 10.10.110.50
Host is up (0.037s latency).
All 65535 scanned ports on 10.10.110.50 are in ignored states.
Not shown: 65535 filtered tcp ports (no-response)

Nmap scan report for 10.10.110.62
Host is up (0.025s latency).
Not shown: 65534 filtered tcp ports (no-response)
PORT     STATE SERVICE
8080/tcp open  http-proxy

Nmap scan report for 10.10.110.74
Host is up (0.027s latency).
Not shown: 65533 filtered tcp ports (no-response)
PORT   STATE SERVICE
22/tcp open  ssh
25/tcp open  smtp

Nmap scan report for 10.10.110.88
Host is up (0.069s latency).
Not shown: 65534 filtered tcp ports (no-response)
PORT   STATE SERVICE
80/tcp open  http

Nmap scan report for 10.10.110.231
Host is up (0.027s latency).
Not shown: 65534 filtered tcp ports (no-response)
PORT    STATE SERVICE
443/tcp open  https

Nmap scan report for 10.10.110.242
Host is up (0.048s latency).
Not shown: 65534 filtered tcp ports (no-response)
PORT   STATE SERVICE
80/tcp open  http

Nmap done: 256 IP addresses (9 hosts up) scanned in 119.87 seconds

---
nmap -p- -sS --min-rate 10000 10.10.110.0/24                                                                                                                                                               
Starting Nmap 7.93 ( https://nmap.org ) at 2023-02-10 11:31 EST                                                                                                                                                
Nmap scan report for 10.10.110.2
Host is up (0.024s latency).
All 65535 scanned ports on 10.10.110.2 are in ignored states.
Not shown: 65535 filtered tcp ports (no-response)

Nmap scan report for 10.10.110.13
Host is up (0.11s latency).
Not shown: 65533 filtered tcp ports (no-response)
PORT    STATE SERVICE                              
53/tcp  open  domain                               
443/tcp open  https                                

Nmap scan report for 10.10.110.21
Host is up (0.089s latency).
All 65535 scanned ports on 10.10.110.21 are in ignored states.
Not shown: 65535 filtered tcp ports (no-response)

Nmap scan report for 10.10.110.50
Host is up (0.089s latency).
All 65535 scanned ports on 10.10.110.50 are in ignored states.
Not shown: 65535 filtered tcp ports (no-response)

Nmap scan report for 10.10.110.62
Host is up (0.044s latency).
Not shown: 65534 filtered tcp ports (no-response)
PORT     STATE SERVICE                             
8080/tcp open  http-proxy

Nmap scan report for 10.10.110.74
Host is up (0.044s latency).
Not shown: 65533 filtered tcp ports (no-response)
PORT   STATE SERVICE                               
22/tcp open  ssh                                   
25/tcp open  smtp

Nmap scan report for 10.10.110.88
Host is up (0.044s latency).
Not shown: 65534 filtered tcp ports (no-response)
PORT   STATE SERVICE
80/tcp open  http

Nmap scan report for 10.10.110.231
Host is up (0.050s latency).
Not shown: 65534 filtered tcp ports (no-response)
PORT    STATE SERVICE
443/tcp open  https

Nmap scan report for 10.10.110.242
Host is up (0.049s latency).
Not shown: 65534 filtered tcp ports (no-response)
PORT   STATE SERVICE
80/tcp open  http

Nmap done: 256 IP addresses (9 hosts up) scanned in 136.06 seconds

---
Nmap scan report for 10.10.110.88
Host is up (0.044s latency).
Not shown: 65534 filtered tcp ports (no-response)
PORT   STATE SERVICE
80/tcp open  http

Nmap scan report for 10.10.110.231
Host is up (0.050s latency).
Not shown: 65534 filtered tcp ports (no-response)
PORT    STATE SERVICE
443/tcp open  https

Nmap scan report for 10.10.110.242
Host is up (0.049s latency).
Not shown: 65534 filtered tcp ports (no-response)
PORT   STATE SERVICE
80/tcp open  http

Nmap done: 256 IP addresses (9 hosts up) scanned in 136.06 seconds

---
nmap -sCV -p8080 10.10.110.62                                                                                                                                                                              
Starting Nmap 7.93 ( https://nmap.org ) at 2023-02-10 11:36 EST                                                                                                                                                
WARNING: Service 10.10.110.62:8080 had already soft-matched rtsp, but now soft-matched sip; ignoring second value                                                                                              
Nmap scan report for 10.10.110.62                                                                                                                                                                              
Host is up (0.018s latency).                                                                                                                                                                                   
                                                                                                                                                                                                               
PORT     STATE SERVICE VERSION                                                                                                                                                                                 
8080/tcp open  rtsp                                                                                                                                                                                            
| fingerprint-strings:                                                                                                                                                                                         
|   FourOhFourRequest, GetRequest, HTTPOptions:                                                                                                                                                                
|     HTTP/1.0 404 Not Found                                                                                                                                                                                   
|     Content-Type: text/html                                                                                                                                                                                  
|     X-Frame-Options: DENY                                                                                                                                                                                    
|     Content-Length: 179                                                                                                                                                                                      
|     X-Content-Type-Options: nosniff                                                                                                                                                                          
|     <!doctype html>                                                                                                                                                                                          

...

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 13.23 seconds

---
nmap -sCV -p22,25 10.10.110.74
Starting Nmap 7.93 ( https://nmap.org ) at 2023-02-10 11:39 EST
Nmap scan report for 10.10.110.74
Host is up (0.14s latency).

PORT   STATE SERVICE VERSION
22/tcp open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 b943bcba43cc2c6ed4fcd5bcc50105af (RSA)
|   256 02abaa0164dec5892f75e36aa9ff78ee (ECDSA)
|_  256 9ac2d3a0fe6aad9a4a850dc115d113be (ED25519)
25/tcp open  smtp    Postfix smtpd
|_smtp-commands: nextcloud, PIPELINING, SIZE 10240000, VRFY, ETRN, ENHANCEDSTATUSCODES, 8BITMIME, DSN, SMTPUTF8
Service Info: Host:  nextcloud; OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 51.40 seconds

---
nmap -sCV -p80 10.10.110.88
Starting Nmap 7.93 ( https://nmap.org ) at 2023-02-10 11:41 EST
Nmap scan report for 10.10.110.88
Host is up (0.018s latency).

PORT   STATE SERVICE VERSION
80/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))
| http-cookie-flags: 
|   /: 
|     PHPSESSID: 
|_      httponly flag not set
|_http-server-header: Apache/2.4.29 (Ubuntu)
|_http-title: DataLeaks

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 12.61 seconds

---
nmap -sCV -p443 10.10.110.231
Starting Nmap 7.93 ( https://nmap.org ) at 2023-02-10 11:44 EST
Nmap scan report for 10.10.110.231
Host is up (0.018s latency).

PORT    STATE SERVICE  VERSION
443/tcp open  ssl/http Apache httpd 2.4.29 ((Ubuntu))
| ssl-cert: Subject: commonName=0x0security.com/organizationName=GiganticHosting CA/stateOrProvinceName=Stockholm/countryName=SE
| Subject Alternative Name: DNS:0x0security.com, DNS:*.0x0security.com
| Not valid before: 2020-03-07T19:45:00
|_Not valid after:  2030-01-07T00:00:00
|_http-server-header: Apache/2.4.29 (Ubuntu)
|_http-title: Promote Business Category Bootstrap Responsive Web Template | ...
| tls-alpn: 
|_  http/1.1
|_ssl-date: TLS randomness does not represent time

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 22.35 seconds

---
nmap -sCV -p80 10.10.110.242
Starting Nmap 7.93 ( https://nmap.org ) at 2023-02-10 11:42 EST
Nmap scan report for 10.10.110.242
Host is up (0.019s latency).

PORT   STATE SERVICE VERSION
80/tcp open  http    Apache httpd 2.4.41 ((Unix))
|_http-title: Gigantic Hosting | Home
| http-methods: 
|_  Potentially risky methods: TRACE
|_http-server-header: Apache/2.4.41 (Unix)

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 12.69 seconds

---
