# Level 13 to 14:
## Level Goal:
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on

## Commands used:
- ls
- ssh – OpenSSH remote login client
- exit

## Solution:
![](./images/13a.jpg)
1. looked into the server and found the key to access the next level
2. tried to log into the next server using the ssh command to no avail, twice, both using the flag -i to recognize the name of the key
3. finally got it by adding the port number 2220 to the command and entered the next level
![](./images/13b.jpg)
![](./images/13c.jpg)

## Links used:
- [Ref](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)
