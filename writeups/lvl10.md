# Level 10 to 11:
## Level Goal:
The password for the next level is stored in the file data.txt, which contains base64 encoded data

## Commands used:
- ls
- cat
- base64 - encodes binary strings into text representations using the base64 encoding format
- exit

## Solution:
![](./images/10.jpg)
1. read up on the base64 command as it would be needed according to the question
2. used the ls command to find the data.txt file
3. used cat on it without base64 utility to see the output
4. used cat again with base64 along with the -d flag to decode the data given in the file
5. found the password and exited to access the next level

## Links used:
- [Ref1](https://en.wikipedia.org/wiki/Base64)
- [Ref2](https://linuxhint.com/bash_base64_encode_decode/)
