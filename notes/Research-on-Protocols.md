---
title: Research on Protocols
publishedAt: 2023-09-06T01:00:00
updatedAt: 2023-09-06T01:00:00
type:
  - Note
published: true
tags:
  - log/learning
---
# Web One

The history of web protocols is a vast topic, and it traces back the origins of how data is transferred over the web. The phrase "Web 1.0" refers to the first iteration of the World Wide Web, characterized by static pages and basic interactivity. The protocols underpinning Web 1.0 primarily include:

## 1. **HTTP (HyperText Transfer Protocol)**:
- **Origins**: Developed by Tim Berners-Lee at CERN in the early 1990s.
- **Function**: HTTP serves as the foundation of any data exchange on the Web. It defines how messages are formatted and transmitted and what actions web servers and browsers should take in response to various commands.
- **HTTP/0.9**: This was the first version, limited and meant for transferring HTML documents only.
## 2. **HTML (HyperText Markup Language)**:
- **Origins**: Also developed by Tim Berners-Lee.
- **Function**: HTML is the standard markup language used to create web pages. It tells the web browser how to structure the content on web pages.
## 3. **URL (Uniform Resource Locator)**:
- **Origins**: Again, credited to Tim Berners-Lee and the early World Wide Web consortium.  
- **Function**: A URL is a reference or address that can be used to access a resource on the web. It specifies the location of a resource and the protocol for accessing it.
## 4. **FTP (File Transfer Protocol)**:
- **Origins**: Pre-dates the World Wide Web and was introduced in the 1970s.
- **Function**: FTP is used to transfer files between computers on a network. It became an essential protocol to upload files (e.g., HTML pages) to web servers.  
### 5. **TCP/IP (Transmission Control Protocol/Internet Protocol)**:
- **Origins**: Developed in the 1970s as a part of the DARPA-sponsored research.
- **Function**: While not exclusive to Web 1.0 or the WWW, TCP/IP is the backbone suite of communication protocols for the Internet. It facilitates end-to-end communication specifying how data should be packaged, addressed, transmitted, routed, and received.
### 6. **SSL (Secure Sockets Layer)**:
- **Origins**: Developed by Netscape in the mid-1990s.
- **Function**: SSL is a security protocol that provides privacy and data integrity between two communicating applications (e.g., a web server and a browser). It's the precursor to TLS (Transport Layer Security).
### 7. **CGI (Common Gateway Interface)**:
- **Origins**: Introduced in the early 1990s.
- **Function**: CGI provides a standard protocol for web servers to execute programs (like console applications) that execute on a server, generating dynamic content.
### 8. **DNS (Domain Name System)**:
- **Origins**: Introduced in the 1980s.
- **Function**: DNS translates domain names to IP addresses so browsers can load resources. It's essentially the phonebook of the internet.



```dataview
TABLE type

FROM "/"

WHERE contains(tags, "protocols")
```
