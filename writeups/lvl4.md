# Level 4 to 5:
## Level Goal:
The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

## Commands used:
- ls
- cd 
- cat
- man – get a manual for the command in question
- file – determine file type
- reset – resets command window
- exit

## Solution:
![](./images/4a.jpg)
![](./images/4b.jpg)
1. used ls to find the inhere directory and entered it
2. used ls within the directory to find 10 different files within it

### method 1: 
3. went through each individual files using cat ./<filenumber> from 0-2 and then backwards from 7-9
4. accidentally stumbled upon the password in file number 7
5. reset the system to try and find a more efficient way

### method 2:
6. looked at a manual of file and used ./* to return the type of data stored in each file
7. file07 stored an ascii value and was the odd one out
8. used the cat command on file07 and found the password
9. exited the server and moved to the next level

## Links used:
- [Ref](https://www.javatpoint.com/linux-file?source=post_page-----72757d03001f--------------------------------)

