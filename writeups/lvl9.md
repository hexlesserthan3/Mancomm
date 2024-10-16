# Level 9 to 10:
## Level Goal:
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

## Commands used:
- ls
- cat
- reset
- grep
- strings - return each string type of characters that are printable in the file
- exit

## Solution:
![](./images/9.jpg)
1. used ls and cat commands to no avail (encountered a block of text)
![](./images/9b.jpg)
![](./images/9c.jpg)
2. reset the window and re-entered the ls command
3. used the cat command with grep = as per the directive
4. got an error of some sort so read up on the strings utility that was on the list of suggested commands
5. decided to try it and entered it as a utility of the cat command alongside grep, using the flag -e as suggested in the second link given below (encoding)
6. got an output of a block of text but noticed the words password and something that appeared to be a correct flag next to a lot of ==’s
7. re-read the question and realized the password would be next to several =’s not one
8. re-entered the cat command as before and added an extra = to find the password
9. exited the server and accessed the next level

## Links used:
- [Ref 1](https://www.educba.com/linux-string-command/)
- [Ref 2](https://www.tutorialspoint.com/unix_commands/strings.htm?source=post_page-----de8c95ce4efc--------------------------------)
