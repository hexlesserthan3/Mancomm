# Level 12 to 13:
## Level Goal:
The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Commands used:
- ls
- cat
- mkdir – make a directory
- xxd – make a hexdump or convert hexdump to binary
- file
- gzip – compress or expand files
- bzip2 – file compressor (block sorting)
- cp – copy files and directories
- mv – rename files 
- exit

## Solution:
![](./images/12a.jpg)
1. looked into the provided file using cat. tried to reverse hexdump the file given but did not have permission to do so
2. made a new directory named tmp/new_dir and copied all the data from the main directory into this one. then moved all the data from data.txt to a file named ‘data’.
 ``` bash
bandit12@bandit:/tmp/new_dir$ cp ~/data.txt
bandit12@bandit:/tmp/new_dir$ ls data.txt
bandit12@bandit:/tmp/new_dir$ mv data.txt data
bandit12@bandit:/tmp/new_dir$ ls data
 ```
3. it started getting too messy so I reset the server and exited in the hopes of trying again and remaking a new directory (which is why there is no screenshot of the above commands since I forgot reset would make all of it disappear)
4. unfortunately, got the output ‘cannot create directory: file exists’ on both my names (random and random_dir) so I decided to try and enter a dir i already knew existed (new_dir) 
![](./images/12b.jpg)
5. used cd to enter the new directory new_dir and look at the file there (data). then used the xxd command on it, but added a flag -r to make sure it understood to convert the data to binary
6. when we look into the directory again we can see two files now: data and binary
7. decided to look at binary, used file command, which told me that binary was gzipped. changed the file extension to fit the requirements to unzip it (changed the suffix to .gz), and used the gzip command with -d flag to decode it.
8. check on the binary file again and this time it’s a bzip2 of compressed data.  decoded that directly which led to another gzip file
![](./images/12c.jpg)
9. repeated steps 7 and 8, along with the tar command with the -xf flag, to keep breaking into the zipped files until finally we get the output ‘data8.bin: ASCII text’.
![](./images/12d.jpg)
![](./images/12e.jpg)
10. cat data8.bin to find the password required, exit and log onto the next level

## Links used:
- [Ref1](https://linuxize.com/post/gzip-command-in-linux/?source=post_page-----2ec761a88907--------------------------------)
- [Ref2](https://linuxize.com/post/how-to-create-and-extract-archives-using-the-tar-command-in-linux/?source=post_page-----2ec761a88907--------------------------------)
