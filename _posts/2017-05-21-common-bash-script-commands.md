---
layout: post
title:  "common bash script commands"
date:   2017-05-21 14:32:04 +0700
categories: [bash, linux]
---

#### Examples
```text
#list file in folder
find .git/objects/ -type f
#find files like pattern in folder
find /tmp -type f -iname "*filename.png"

#filter list file in more files with pattern [7660]
grep -l "7660" /tmp/*
#search text in folders:	
grep -R "ドラゴンオーブ" /tmp

#open file f1.txt, replace 'f1' to 'datdao', output new file name 'f1_new.txt'
cat f1.txt | sed 's/f1/datdao/g' > f1_new.txt
#replace content in file 'f1.txt': from 'datdao' to 'f1xx'
sed -i -e 's/datdao/f1xx/g' f1.txt

#get current datetime and write in the file with format: 2018-12-13 17:02:19
echo `date '+%Y-%m-%d %H:%M:%S'` > current_datetime.txt

#debug process in linux
#find pid of process
sudo ps -ef |grep apache2
sudo lsof -p 11685 #pid's apache2

sudo lsof |grep "mysql"
sudo lsof |grep "apache"
sudo lsof |grep php
sudo lsof |grep apache
```

```text
ls: Show directory contents, lists names of files.
mkdir: Creates a directory of the specified name.
cat: Display contents of a file.
cd: Change directory. Change to certain directory name if provided.
pwd: Displays the name of the working directory.
touch: Creates a blank file with a specified name.
less: View contents of specified file, page by page.
head/tail: Displays the first/ last 10 lines of a file.
rm: Removes a specified file. This action is permanent. There is no recycle bin.
rmdir: Removes a directory.
history: Display a listing of the last commands you've run.
cp: Copy specified file to a new named file. Use -r flag to copy a directory.
mv: Rename a specified file or directory.
find: search files and directories. Can use with wildcards (* ? [ ]).
quota: Print the amount of space available and used on all shares for the current user.
scp: Secure/ SSH copy. Copies from either the local filesystem to a remote filesystem
```
if...then...else
```
if [command]
then
    commands
else
    commands
fi - opposite of if. It signifies the end of the if...then statement.
```
Input/ Output Redirection

Bash uses three main streams of data: input, output and error. You can direct input and output of data with various commands.
```txt
< : Takes the contents out of the file and redirects it to the program.
> : Takes the STDOUT (output stream) of the specified program, and writes it to a certain file. Any contents already in the file are overwritten.
>> : Takes the STDOUT of the specified program and appends (adds) it to the specified program. The original contents of the file remain, instead of being deleted.
| : Takes the output of a specified program and redirects it as input to another program (called piping).

```

Wildcards act as substitutions for character strings. They can be used with search and other functions.
```
*: zero or more characters.
?: any one character
[ ]: any character within the brackets
Example: rm *.o would remove all files that ended with .o in a directory.
```

**Refference:** [https://www.unr.edu/research-computing/the-grid/using-the-grid/bash-commands](https://www.unr.edu/research-computing/the-grid/using-the-grid/bash-commands)

hope it usefull.
