# Level 17 to 18:
## Level Goal:
There are 2 files in the home directory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new

## Commands used:
- ls
- cat
- diff – compares text files
- exit

## Solution:
1. used cat to get the password for the level similar to level 15. 
2. used ls to see the files in directory
3. looked into one of the files using cat and found a block of text
![](./images/17a.jpg)
4. looked up how to figure out what’s the difference between two files, found the diff command
5. used the diff command to find the two differences in the file
6. stored both the files in my notepad but used only the ‘passwords.new’ password to log onto the next level according to the question
![](./images/17b.jpg)

## Links used:
- [Ref](https://www.ibm.com/docs/en/aix/7.2?topic=files-comparing-diff-command)
