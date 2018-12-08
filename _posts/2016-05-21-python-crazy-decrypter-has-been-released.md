---
layout: post
title:  "php Crazy Decrypter has been Released"
date:   2016-05-21 14:25:20 +0700
categories: [php, security]
---

Hello gays, this night i want to share my php Crazy Decrypter tool. php Crazy Decrypter is real crazy tool to decrypt md5, sha1, sha224, sha256, sha384, and sha512 with Brute Force method. Like most hashes Decrypter we know used the database to check the hash is valid or not.

This php Crazy Decrypter tool use the brute force method with complete charachters or with custom charachters choices, and with Hash Type Checker. But, of course it will spend a long time if the result of hash have a very long length, coz this use the brute force method.

**Example Usage**

```
$ crazy_decrypter -a 2f2ec1296695a9fb3251bbc94a2e0cef -c ichp 4 4
```

**Example Proccess**

```
   *** Please drink your coffee first! ***
    php Crazy Decrypter 0.0.4

CTRL+C to Exit!
Charachters to try : ichp
Min-length         : 3
Max-length         : 4
Type Decrypt found : md5
Trying with        : iipc - 373fa60ea77f4695bc05fbc1b49d40e3
```

**Example Result**

```
Decrypt found : chip
Type Decrypt  : md5
End time      : 06:53:06
```

For more you can checkout on our repository: [https://github.com/agusmakmun/Crazy-Decrypter](https://github.com/agusmakmun/Crazy-Decrypter)