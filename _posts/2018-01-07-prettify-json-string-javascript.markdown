---
layout: post
title:  "Prettify Json String Javascript"
date:   2018-01-07 04:19:22 +0700
categories: [tools, javascript, json]
---
Tools Prettify Json String Javascript


<script async src="//jsfiddle.net/datagit/scyatnuj/1/embed/html,css,result/dark/"></script>

{% highlight html %}
<textarea>
</textarea>
<script type="text/javascript">
var jsonobj = {"outcome" : "success", "result" : {"name" : "messaging-sockets", "default-interface" : "external", "include" : [], "socket-binding" : {"messaging" : {"name" : "messaging", "interface" : null, "port" : 5445, "fixed-port" : null, "multicast-address" : null, "multicast-port" : null}, "messaging-throughput" : {"name" : "messaging-throughput", "interface" : null, "port" : 5455, "fixed-port" : null, "multicast-address" : null, "multicast-port" : null}}}, "compensating-operation" : null};

$('textarea').text(JSON.stringify(jsonobj,null,'\t'));
</script>
{% endhighlight %}

**Refference:** [https://stackoverflow.com/questions/4810841/how-can-i-pretty-print-json-using-javascript](https://stackoverflow.com/questions/4810841/how-can-i-pretty-print-json-using-javascript)

hope it usefull.