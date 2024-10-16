# Level 3 to 4:
## Level Goal:
The password for the next level is stored in a hidden file in the inhere directory

## Commands used:
- ls
- cd – change the working directory
- cat
- exit

## Solution:
![](./images/3.jpg)
1. used ls to find the directory mentioned
2. used the cd command to enter the inhere directory
3. used ls again to get no output
4. looked into the ls manual to find the -a flag to view all files including hidden ones
5. the output arrives as ‘. .. .hidden’ and we can see .hidden is the file needed
6. use the command cat on that file and find the password
7. exit the server and access the next level

## Links used:
- [Ref](https://man7.org/linux/man-pages/man1/ls.1.html)

