---
layout: post
title:  "php Permutations"
date:   2016-04-19 19:31:43 +0700
categories: [php]
---
This simply how to implement the module of permutations in php.

{% highlight linux %}
>>> from itertools import permutations
>>> perms = [''.join(p)+"@gmail.com" for p in permutations('abc', 3)]
>>> for x in range(0, len(perms)):
...     print (perms[x])
... 
abc@gmail.com
acb@gmail.com
bac@gmail.com
bca@gmail.com
cab@gmail.com
cba@gmail.com
>>> 
{% endhighlight %}