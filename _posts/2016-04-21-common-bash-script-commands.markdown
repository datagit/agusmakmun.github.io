---
layout: post
title:  "Common Bash Script Commands"
date:   2016-04-21 19:31:43 +0700
categories: [bash, linux]
---

#### Examples

#### list file in folder
```bash
$ find .git/objects/pack -type f
```
output on terminal
```bash
.git/objects/pack/pack-851ddc2ab8845e7fad3320bf376c3ac534a0cea6.idx
.git/objects/pack/pack-851ddc2ab8845e7fad3320bf376c3ac534a0cea6.pack
.git/objects/pack/pack-902a1cdc92b6aca4b85fd87fff77d04934ea7150.idx
.git/objects/pack/pack-902a1cdc92b6aca4b85fd87fff77d04934ea7150.pack
```
```bash
#find files like pattern in folder
$ find .git/objects/pack/ -type f -iname "*851d*"
```
output on terminal
```bash
.git/objects/pack/pack-851ddc2ab8845e7fad3320bf376c3ac534a0cea6.idx
.git/objects/pack/pack-851ddc2ab8845e7fad3320bf376c3ac534a0cea6.pack
```

```bash
#filter list file in more files with pattern [7660]
grep -l "7660" /tmp/*
#search text in folders:   
grep -R "abc" /tmp

#open file f1.txt, replace 'f1' to 'datdao', output new file name 'f1_new.txt'
cat f1.txt | sed 's/f1/datdao/g' > f1_new.txt
#replace content in file 'f1.txt': from 'datdao' to 'f1xx'
sed -i -e 's/datdao/f1xx/g' f1.txt

#get current datetime and write in the file with format: 2018-12-13 17:02:19
echo `date '+%Y-%m-%d %H:%M:%S'` > current_datetime.txt
```

#### debug process in linux
```bash

#find pid of process
sudo ps -ef |grep apache2
sudo lsof -p 11685 #pid's apache2

sudo lsof |grep "mysql"
sudo lsof |grep "apache"
sudo lsof |grep php
sudo lsof |grep apache
```

**Refference:** [https://www.unr.edu/research-computing/the-grid/using-the-grid/bash-commands](https://www.unr.edu/research-computing/the-grid/using-the-grid/bash-commands)

hope it usefull.
