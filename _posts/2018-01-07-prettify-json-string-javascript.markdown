---
layout: post
title:  "Prettify Json String Javascript"
date:   2018-01-07 04:19:22 +0700
categories: [tools, javascript, json]
---
Tools Prettify Json String Javascript

<iframe width="100%" height="500" src="//jsfiddle.net/datagit/scyatnuj/1/embedded/result/dark/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

{% highlight html %}
<textarea id="input" rows="3" cols="80"></textarea>
<button onclick="main();">
Submit
</button>
<pre id="output"></pre>
<script>
function output(inp) {
document.getElementById("output").innerHTML = inp;
}

function syntaxHighlight(json) {
    json = json.replace(/&/g, '&amp;').replace(/</g, '&lt;').replace(/>/g, '&gt;');
    return json.replace(/("(\\u[a-zA-Z0-9]{4}|\\[^u]|[^\\"])*"(\s*:)?|\b(true|false|null)\b|-?\d+(?:\.\d*)?(?:[eE][+\-]?\d+)?)/g, function (match) {
        var cls = 'number';
        if (/^"/.test(match)) {
            if (/:$/.test(match)) {
                cls = 'key';
            } else {
                cls = 'string';
            }
        } else if (/true|false/.test(match)) {
            cls = 'boolean';
        } else if (/null/.test(match)) {
            cls = 'null';
        }
        return '<span class="' + cls + '">' + match + '</span>';
    });
}
function main() {
    var obj = {a:1, 'b':'foo', c:[false,'false',null, 'null', {d:{e:1.3e5,f:'1.3e5'}}]};
    var input = document.getElementById("input").value;
	  if (input != '') {
  	  obj = JSON.parse(input);
  	}
  	var str = JSON.stringify(obj, undefined, 4);   
  	//output(str);
  	output(syntaxHighlight(str));

}


</script>
{% endhighlight %}

**Refference:** [https://stackoverflow.com/questions/4810841/how-can-i-pretty-print-json-using-javascript](https://stackoverflow.com/questions/4810841/how-can-i-pretty-print-json-using-javascript)

hope it usefull.