---
layout: post
title:  "File Permissions In Linux"
date:   2018-01-07 19:31:43 +0700
categories: [bash, linux]
---

#### This lesson will cover the following commands:

- chmod - modify file access rights
- su - temporarily become the superuser
- sudo - temporarily become the superuser
- chown - change file ownership
- chgrp - change a file's group ownership


| Value	| Meaning |
| ----- | ------- |
| 777	| (rwxrwxrwx) No restrictions on permissions. Anybody may do anything. Generally not a desirable setting. |
| 775   | (rwxr-xr-x) The file's owner may read, write, and execute the file. All others may read and execute the file. This setting is common for programs that are used by all users. |
| 700   | (rwx------) The file's owner may read, write, and execute the file. Nobody else has any rights. This setting is useful for programs that only the owner may use and must be kept private from others. |
| 666   | (rw-rw-rw-) All users may read and write the file. |
| 644   | (rw-r--r--) The owner may read and write a file, while all others may only read the file. A common setting for data files that everybody may read, but only the owner may change. |
| 600   | (rw-------) The owner may read and write a file. All others have no rights. A common setting for data files that the owner wants to keep private. |


Here we can see:

- The file "/bin/bash" is owned by user "root"
- The superuser has the right to read, write, and execute this file
- The file is owned by the group "root"
- Members of the group "root" can also read and execute this file
- Everybody else can read and execute this file


```bash
#file
[me@linuxbox me]$ ls -l /bin/bash
-rwxr-xr-x 1 root root  316848 Feb 27  2000 /bin/bash
```
![describe](http://linuxcommand.org/images/file_permissions.png)

```bash
#dictionary
$ ls -l app/
total 8
drwxr-xr-x  3 datdm  staff  102 Dec 16 15:34 Console
drwxr-xr-x  3 datdm  staff  102 Dec 16 15:34 Exceptions
drwxr-xr-x  5 datdm  staff  170 Dec 16 15:34 Http
-rw-r--r--  1 datdm  staff  100 Dec 16 15:34 Post.php
drwxr-xr-x  7 datdm  staff  238 Dec 16 15:34 Providers
-rw-r--r--  1 datdm  staff  558 Dec 16 15:34 User.php
```
chmod

It is easy to think of the permission settings as a series of bits (which is how the computer thinks about them). Here's how it works:

```
rwx rwx rwx = 111 111 111
rw- rw- rw- = 110 110 110
rwx --- --- = 111 000 000

#and so on...

rwx = 111 in binary = 7
rw- = 110 in binary = 6
r-x = 101 in binary = 5
r-- = 100 in binary = 4
```

**Refference:** [http://linuxcommand.org/lc3_lts0090.php](http://linuxcommand.org/lc3_lts0090.php)

hope it usefull.
