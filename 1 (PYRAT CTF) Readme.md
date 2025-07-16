# ctf-journey

# PYRAT CTF CHALLENGE

![image](https://github.com/idevyogi/ctf-journey/blob/1d2e7439ec3c447fea1c18a03770848f0baff211/Screenshot%202025-07-16%20164113.png)
![image](https://raw.githubusercontent.com/idevyogi/ctf-journey/5177707821f5c48910197600dc368d8e2d22ad02/PYRAT%20CTF%20CHALLENGE.png)

# step 1 rustscan 

PORT     STATE SERVICE  REASON
22/tcp   open  ssh      syn-ack ttl 60
8000/tcp open  http-alt syn-ack ttl 60

i cant go on ssh because i have zero information about credentials
so i browse port 8000 in fire fox browser

# step 2 http://10.10.121.147:8000/
Try a more basic connection! 


TCP ya UDP connection banaana, jisme data end-to-end stream ke form me exchange hota hai — bina kisi extra formatting ke.

# step 3  Usage of NETCAT for basic connection
nc <target_ip> <port>

(idevyogi㉿kali)-[~]
└─$ nc 10.10.121.147 8000
after this i got my cursor in next line and just blank theen i give hello nomral in it then it respond to me in this way
REASON OF HELLO -
✅ Agar reply milta hai, to samajh aata hai ki port alive aur responsive hai
hello
name 'hello' is not defined


# step 4 as i know defined error is given in programming python so i try their code
print(1+1)
2
it works so now i will give input of python to retrieve information



