# Logging For Fun and Profit 
Andy Hakala - Systems Engineer

+++

## About Me
 - System Engineer that likes to write code
 - Enjoy problem solving

---

## __Logging__
### The way that systems keep track of what happened, when it happened, and by whom
---
@snap[west span-55]
## Who is interested in logs?
@snapend
@snap[east span-45]
@ul
 - System Admins
 - Software Engineers
 - Other systems
 - ...*and even more*!
 - Executives 
 - "Bad Guys"
@ulend
@snapend

---

## When is this stuff valueable?
@ul 
 - When something unexpected happens
 - To confirm something expected actually happened
 - To better understand how things happen
 - To better predict what might be

+++
### Example - Web Logs
```
208.115.111.72 - - [17/May/2015:11:05:26 +0000] "GET /blog/rants/fedora-yum.html HTTP/1.1" 200 8328 "-" "Mozilla/5.0 (compatible; Ezooms/1.0; help@moz.com)"
208.115.111.72 - - [17/May/2015:11:05:32 +0000] "GET /blog/tags/grok HTTP/1.1" 200 30346 "-" "Mozilla/5.0 (compatible; Ezooms/1.0; help@moz.com)"
208.115.111.72 - - [17/May/2015:11:05:12 +0000] "GET /blog/tags/is%20it%20done%20yet HTTP/1.1" 200 10544 "-" "Mozilla/5.0 (compatible; Ezooms/1.0; help@moz.com)"
208.115.111.72 - - [17/May/2015:11:05:07 +0000] "GET /blog/tags/statistics HTTP/1.1" 200 29706 "-" "Mozilla/5.0 (compatible; Ezooms/1.0; help@moz.com)"
50.180.79.170 - - [17/May/2015:11:05:50 +0000] "GET /favicon.ico HTTP/1.1" 200 3638 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10.5; rv:16.0) Gecko/20100101 Firefox/16.0"
```



