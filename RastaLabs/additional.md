WS01 pvQs56A1     
WS01              
WS02 65arknoC     
WS02              
WS03 okPcK70J     
WS03              
WS04 OX6O39k1     
WS04              
WS05 oRSyj65W     
WS05              
WS06 0Sgz7kt9     
WS06 

$secpassword = convertto-securestring "OX6O39k1" -asplaintext -force
$cred = new-object system.management.automation.pscredential('ws04\administrator', $secpassword)
invoke-command -computername ws04 -credential $cred -scriptblock {ipconfig}

Get-EventLog -LogName "Application" | where {$_.Message -like 'RASTA{'} | select Message | format-table -wrap

Get-EventLog -LogName "Application"|select -expandproperty Message > test.txt

get-childitem -path c:\ -include *.bat -recurse -force -erroraction 'silentlycontinue'

Get-EventLog -LogName "Active Directory Web Services"  | where {$_.Message -like 'RASTA{'}

Get-EventLog -LogName "Application" | findstr 'RASTA{'