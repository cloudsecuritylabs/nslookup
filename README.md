# nslookup
nslookup
```
nslookup /?
```

## Non Interactive Mode
```
nslookup www.google.com
DNS server is typically ISP provided router on private IP
For authoritative response, DNS server must be responsible for the domain
```

```
nslookup -type=mx cnn.com 8.8.8.8
-type=mx is used to search for mail exchange servers usign the DNS server @ 8.8.8.8
```

## Interactive Mode
~~~
nslookup
set type=mx [or set q=mx]
server 8.8.8.8
google.com
~~~

## extended nslookup
```
nslookup
set debug
set type=aaaa
google.com


nslookup
set debug
set type=mx
google.com

nslookup
set debug
set type=ns
google.com

nslookup
set debug
set type=txt
google.com
```

## zone transfer
```
nslookup
website.com
server [ns serer of website]
type=ANY
ls -d google.com
```
