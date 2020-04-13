### Difference between an application and a service
-- Can think of an application as a program that runs on the client side whenever the user wants to use that program.
-- A service on the other hand is something that's always running on a server and is expecting to serve all users on that 
server that request the use of that service. 
-- So that's why like from a web development server side perspective you see that certain services are down.
Hmm, but I can also say that the application google is down say. 
So what another thing is an application is user facing while a service is not user facing but is something
that is used by application.

### A question I had was how is the HTTP status response returned in a HTTP response?
-- I was thinking the status code is another key value pair in the header. 
-- But no, the status code is returned in the status line.
-- What you have is the status line, the headers (and there are three types of headers-- general, response and entity) and the message body as defined per the RFC for HTTP:
https://www.w3.org/Protocols/rfc2616/rfc2616-sec6.html

```
Response      = Status-Line               ; Section 6.1
                       *(( general-header        ; Section 4.5
                        | response-header        ; Section 6.2
                        | entity-header ) CRLF)  ; Section 7.1
                       CRLF
                       [ message-body ]          ; Section 7.2
```                      
```Status-Line = HTTP-Version SP Status-Code SP Reason-Phrase CRLF```
```
response-header = Accept-Ranges           ; Section 14.5
                       | Age                     ; Section 14.6
                       | ETag                    ; Section 14.19
                       | Location                ; Section 14.30
                       | Proxy-Authenticate      ; Section 14.33
                       | Retry-After             ; Section 14.37
                       | Server                  ; Section 14.38
                       | Vary                    ; Section 14.44
                       | WWW-Authenticate        ; Section 14.47
```
Even better general purpose explanation of the format of a HTML request/response message packet:
https://en.wikipedia.org/wiki/HTTP_message_body
```
The request/response message consists of the following:

Request line, such as GET /logo.gif HTTP/1.1 or Status line, such as HTTP/1.1 200 OK,
Headers
An empty line
Optional HTTP message body data
The request/status line and headers must all end with <CR><LF> 
(that is, a carriage return followed by a line feed). 
The empty line must consist of only <CR><LF> and no other whitespace.
```

### Sessions and Cookies

So session and cookie management goes into a lot of detail and there are a number of approaches and number a security concerns 
to be conversant with when on the topic of session and cookie management. 
It's a big topic and has a lot of details to it. 

At a very high level, sessions and cookies are a mechanism for creating stateful web applications using a statless protocol 
such as HTTP. 
Sessions are stored on the server side and each session has a session identifier and this session identifier is sent to and 
stored on the client side, in the browser as cookies. The browser application allows for cookies to be sent from the server and 
set for that browser/user agent. And the browser then sends that cookie which is used as a session id to the server on all sub-
sequent requests from the browser. 

There are different types of cookies which do different things. So yeah this goes a lot in depth. 

Just this page https://launchschool.com/books/http/read/statefulness is only an overview. 

In depth study of cookies and sessions needs to start from the MDN page:
https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies 

And then there are some other resource that may make sense as we read some more.
https://www.guru99.com/difference-between-cookie-session.html
https://stackoverflow.com/questions/6253633/cookies-vs-sessions
https://security.stackexchange.com/questions/92122/why-is-it-insecure-to-store-the-session-id-in-a-cookie-directly
https://medium.com/@sherryhsu/session-vs-token-based-authentication-11a6c5ac45e4
https://web.stanford.edu/~ouster/cgi-bin/cs142-fall10/lecture.php?topic=cookie
