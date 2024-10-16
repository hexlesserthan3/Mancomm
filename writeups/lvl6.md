# Level 6 to 7:
## Level Goal:
The password for the next level is stored somewhere on the server and has all of the following properties:
- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

## Commands used:
- ls
- cat
- find
- exit

## Solution:
![](./images/6a.jpg)
![](./images/6b.jpg)
1. used ls command to get no output
2. used find with the given specifications to get a long list of files which I was denied permission to
3. while scrolling down it, realized that one of the files did not have a permission denied next to it 
4. decided to concatenate that file and found the password
5. exited the server and accessed the next level

## Links used: none
### Note: want to know if there is a way to acquire only the file I have been given access to, rather than having to go through all the files and spot one by chance.

