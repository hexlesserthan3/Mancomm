# Level 8 to 9:
## Level Goal:
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

## Commands used:
- ls
- cat
- uniq – reports or filters out the repeated lines in a file
- sort – sorts the data given
- exit

## Solution:
![](./images/8a.jpg)
1. used the ls command to find the data.txt file and concatenated it
2. found a huge block of data
3. read up on the uniq utility and ran it as a part of the cat command, with the flag -u to find the unique line of data 
4. got the same block of data (no noticeable difference)
5. re-read the function of uniq utility and realized that it only works on sorted data
![](./images/8b.jpg)
![](./images/8c.jpg)
6. used the cat command with both the sort and uniq utilities (with -u flag) and found the password
7. exit the server and entered the next level

## Links used:
- [Ref](https://www.geeksforgeeks.org/uniq-command-in-linux-with-examples/)
