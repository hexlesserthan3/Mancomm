# Level 18 to 19:
## Level Goal:
The password for the next level is stored in a file readme in the home directory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.

## Commands used:
- ls
- cat
- diff – compares text files
- exit

## Solution:
![](./images/18a.jpg)
![](./images/18b.jpg)

### Method 1:
1. saw that I can’t log onto the localhost even with the right password
2. decided to look up how to circumvent the problem
3. decided to execute commands within the ssh command
4. used ls within the ssh command and found the readme file
5. used cat readme within the ssh command once more and found the password
![](./images/18c.jpg)

### Method 2:
6. while looking up ways to circumvent the problem, realized that I could also use a preset shell to log into the server, with a -t flag to specify that the shell will be used to log into the server
7. decided to use the /bin/sh shell since that was the one that seemed most common in the details of all the shells stored in linux
8. further, used ls and cat after successfully logging into the server to find the password and exited the server
![](./images/18d.jpg)

## Links used:
- [Ref1](https://www.cyberciti.biz/faq/unix-linux-execute-command-using-ssh/)
- [Ref2](https://serverfault.com/questions/162018/force-ssh-to-use-a-specific-shell)
- [Ref3](https://medium.com/@JAlblas/tryhackme-what-the-shell-walkthrough-6c0ebe8f854e)

