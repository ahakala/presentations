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
@ulend
@snapend

---

## When is this stuff valuable?
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


---
How this often gets consumed
![](logging/assets/img/Logging.png)

+++

@snap[east span-45]
![](logging/assets/Logging.png)
@snapend
@snap[west span-55]
### Problems with this
 - no global view
 - encourages hero culture
 - each team (or individual) has a unique practice

---
A better way...

![](logging/assets/img/Log-Agg.png)

+++
@snap[north]
### Why this is better
@snapend
@snap[south-west span-45]
![](logging/assets/img/Log-Agg.png)
@snapend
@snap[east span-55]
 - shared view of the system
 - encourages shared practices
 - information valuable in new ways
@snapend
+++
### Now we can use logs for...
 - better understand user experience
 - use data to inform decision making
 - create product objectives based on data
   - _"99% of requests result in HTTP 200 over a 30 day timespan"_

---
## Pactices

---
@size[.5em]("A twelve-factor app never concerns itself with routing or storage of its output stream. It should not attempt to write to or manage logfiles. Instead, each running process writes its event stream, unbuffered, to stdout. During local development, the developer will view this stream in the foreground of their terminal to observe the app’s behavior. In staging or production deploys, each process’ stream will be captured by the execution environment, collated together with all other streams from the app, and routed to one or more final destinations for viewing and long-term archival. These archival destinations are not visible to or configurable by the app, and instead are completely managed by the execution environment." --https://12factor.net/logs)

---
### General Rules 
1. Log to standard out
2. If a file or location must be specified, make it configurable at runtime
3. Don't ship directly from the app to something like Splunk or Elastic 



