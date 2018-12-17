---
layout: post
title:  "List Files And Directories Describe Information"
date:   2018-01-06 19:31:43 +0700
categories: [bash, linux]
---

# ls

The ls command is used to list the contents of a directory. It is probably the most commonly used Linux command. It can be used in a number of different ways. Here are some examples:

Examples of the ls command

| Command                | Result                                 |
| ---------------------- | ---------------------------------------
| ls	                 | List the files in the working directory |
| ls /bin                | List the files in the /bin directory (or any other directory you care to specify) |
| ls -l	                 | List the files in the working directory in long format |
| ls -l /etc /bin	     | List the files in the /bin directory and the /etc directory in long format |
| ls -la ..	             | List all files (even ones with names beginning with a period character, which are normally hidden) in the parent of the working directory in long format | 

## A Closer Look At Long Format

```
-rw-------   1 bshotts  bshotts       576 Apr 17  1998 weather.txt
drwxr-xr-x   6 bshotts  bshotts      1024 Oct  9  1999 web_page
-rw-rw-r--   1 bshotts  bshotts    276480 Feb 11 20:41 web_site.tar
-rw-------   1 bshotts  bshotts      5743 Dec 16  1998 xmas_file.txt

----------     -------  -------  -------- ------------ -------------
    |             |        |         |         |             |
    |             |        |         |         |         File Name
    |             |        |         |         |
    |             |        |         |         +---  Modification Time
    |             |        |         |
    |             |        |         +-------------   Size (in bytes)
    |             |        |
    |             |        +-----------------------        Group
    |             |
    |             +--------------------------------        Owner
    |
    +----------------------------------------------   File Permissions
```

**Refference:** [http://linuxcommand.org/lc3_lts0030.php](http://linuxcommand.org/lc3_lts0030.php)

hope it usefull.
