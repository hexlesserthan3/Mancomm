# Level 16 to 17:
## Level Goal:
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

## Commands used:
- ls
- cat
- touch – tested a name to see if the file or folder is empty
- nmap - network exploration tool and security / port scanner
- ssh
- openssl – openssl command line tool
- s_client – tls client program
- exit

## Solution:
![](./images/16a.jpg)
1. the service that we need is running in the range 31,000–32,000, we can find all services in that range using nmap command with the -p flag is used to specify the ports and the -sV flag to identify the versions of the services
2. if we look at the results more closely, we see that on port 31790 is specified outside the “wrong! Please enter the correct passwords!”
3. using openssl and s_client with the connect flag to connect to localhost:31790, and entered the password that I used to enter into this level
4. here we get an RSA private key. decided to look up how to use RSA keys and found out you can use both vim and nano to copy rsa private keys, and store them in a file
5. touched a tmp directory to see if I could cd into it, and proceeded to enter into it to store the key into a file ‘private.key’ using nano command.
![](./images/16b.jpg)
![](./images/16c.jpg)
![](./images/16d.jpg)
![](./images/16e.jpg)
6. used the ls command with -l flag to look at the permissions of the file since that proved to be a problem before in a previous level, changed the permissions to 400 to make it less public
7. unfortunately, this key did not work and I tried to do the same thing over and over (did not take screenshot as it was all futile attempts with no avail.)
8. looked at every single walkthrough I could find and still did not realize what I was doing wrong
![](./images/16f.jpg)
![](./images/16g.jpg)
9. tried again the next day, this time by changing the permissions to 600 instead of 400 or 700 like I was trying before
10. this finally worked and I was able to log into the bandit17 server and get the password using cat /etc/bandit_pass/bandit17
![](./images/16h.jpg)
![](./images/16i.jpg)

## Links used:
- [Ref1](https://youtu.be/CQ14LbpQofQ?si=P7MfWw7ADitZ4udo)
- [Ref2](https://stackoverflow.com/questions/75935815/stuck-on-16-17-level-of-overthewire-bandit-game)
- [Ref3](https://en.wikipedia.org/wiki/Port_scanner)
- [Ref4](https://www.ssldragon.com/blog/what-is-openssl/)
- [Ref5](https://www.geeksforgeeks.org/practical-uses-of-openssl-command-in-linux/)
- [Ref6](https://www.geeksforgeeks.org/nmap-command-in-linux-with-examples/)
- [Ref7](https://www.openssl.org/docs/man1.1.1/man1/openssl-s_client.html#:~:text=The%20s_client%20command%20implements%20a,diagnostic%20tool%20for%20SSL%20servers)
