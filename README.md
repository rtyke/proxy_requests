## make an http GET/POST with a proxy scraped from https://www.sslproxies.org/
<br><br>
It first scrapes proxies from the web
<br><br>
Then it recursively attempts to make a request if the initial request with a proxy is unsuccessful
<br><br>
Runs on Linux and Windows-<b>may take a moment to run depending on current proxy</b>
<br><br>
Pass it a fully qualified URL when inializing an instance:
<br><br>
EXAMPLE GET:<br>
&emsp;&nbsp;r = ProxyRequests("https://postman-echo.com/get?foo1=bar1&foo2=bar2")<br>
&emsp;&nbsp;r.get()<br>
&emsp;&nbsp;print(r)<br>
&emsp;&nbsp;print(r.to_json())<br>
&emsp;&nbsp;print(r.get_headers())
<br><br>
EXAMPLE POST:<br>
&emsp;&nbsp;r = ProxyRequests("http://ptsv2.com/t/8s8j9-1533491569/post")<br>
&emsp;&nbsp;r.post({"key": "value"})<br>
&emsp;&nbsp;r.post("string here")<br>
&emsp;&nbsp;print(r)<br>
&emsp;&nbsp;print(r.get_headers())
<br><br>
In the URL above... Whomever made ptsv2.com (for testing HTTP requests) is awesome... NO setup and NO accounts needed
<br><br>
This was developed on Ubuntu 16.04.4 LTS.
<br><br>
HTTP Basic Auth subclass coming soon (with overrided methods probably) 
<hr>
<b>Author: James Loye Colley  04AUG2018</b>
