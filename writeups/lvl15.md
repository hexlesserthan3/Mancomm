# Level 15 to 16:
## Level Goal:
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption 

## Commands used:
- ls
- cat
- nc – TCP/IP swiss army knife 
- exit

## Solution:
![](./images/15a.jpg)
![](./images/15b.jpg)
![](./images/15c.jpg)
1. used ls to no output then opened a manual on openssl, used the connect flag to connect to the port given in the question
2. got an output with no instructions so entered a question mark to see the result
3. output was ‘Wrong! Enter the correct password’ and hence, decided to try the same thing as last level
4. got the correct password by rereading the file /etc/bandit_pass/bandit15
5. retried step 1, and this time entered the password and got the password for the next level.
6. Tried a different method using ncat --ssl which did not work (which I now see is because I was entering the wrong port), so decided to just exit out of the server
 
## Links used: 
- [Ref](https://en.wikipedia.org/wiki/Transport_Layer_Security#SSL_1.0,_2.0,_and_3.0)

