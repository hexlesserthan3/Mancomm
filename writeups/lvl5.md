# Level 5 to 6:
## Level Goal:
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
- human-readable
- 1033 bytes in size
- not executable

## Commands used:
- ls
- cd
- cat
- find – finds the file with the given flags/specifications
- exit

Solution:
![](./images/5.jpg)
1. used ls command to find inhere directory
2. entered mentioned directory and used ls command again to find 18 directories
3. decided against using cat on individual directories as in the previous level and follow the limitations given in the question
4. find the file using the file command with the flags mentioned in the question after looking into the working of the find command
5. used the cat command on the file that showed up and found the password
6. exited the server and moved onto the next level

##Links used:
- [Ref](https://www.tecmint.com/35-practical-examples-of-linux-find-command/?source=post_page-----aa853b431c1d--------------------------------)

