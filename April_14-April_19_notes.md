### April 14 Notes

## TCP connection and TLS handshake
So from the networking/protocols simplified chapter of curl book: https://ec.haxx.se/protocols/protocols-curl
an additional piece of learning about how connections between clients and servers is being established.
Once the IP address of the server through the DNS lookup has been obtained there is then the process of establishing 
a TCP connection with the server. In addition to the TCP connection there may need to be a TLS handshake for the secure 
version of the application level protocols.
Once the TCP connection and TLS handshake is established it is then that the client starts communicating with the server 
using whatever the application protocol maybe. 
For browsers it's by default HTTP/S. For CURL it's any one of the protocols that uses the url/uri structure for identifying
servers. Since curl uses the url format for identifying the servers.

Yeah all of these protocols with their corresponding services are being run on well defined, well known ports on the server. 

### So then the question based on that I had yesterday was that, say for a web server, how is it handling thousands 
or millions of requests at the same port?
https://www.google.com/search?q=how+many+request+can+be+served+by+a+server+at+port+80&rlz=1C5CHFA_enUS891US891&oq=how+many+request+can+be+served+by+a+server+at+port+80&aqs=chrome..69i57.14303j0j7&sourceid=chrome&ie=UTF-8
There are a lot of answers. We need to go through them and summarize that.

### Also led to like what exactly is a TLS handshake?
https://www.google.com/search?q=whats+a+TLS+handshake&rlz=1C5CHFA_enUS891US891&oq=whats+a+TLS+handshake&aqs=chrome..69i57j0l7.3703j0j7&sourceid=chrome&ie=UTF-8


### April 15 Notes
This search I had made yesterday but noted down. Which was about trying to understand whether it's the browser that is opening 
the TCP connections.
https://www.google.com/search?q=does+a+browser+create+a+tcp+connection&rlz=1C5CHFA_enUS891US891&oq=does+a+browser+create+a+tcp+connection&aqs=chrome..69i57j33.15727j0j7&sourceid=chrome&ie=UTF-8

This is an interesting question to ask because it leads to the answer of how the browser works for communicating over the network
which is by calling the OS Network APIs. 
So even for the other application layer protocols the browser is invoking the OS APIs for sending packets from the client machine 
to the server and same for as it listens for packets from the server. 
The server sending it to an IP address to a machine. It's not to a browser or a cmd line tool or some other client. It doesn't 
know about the program that's requesting the packet on the client machine. 
So this is why there's the user-agent header in HTTP packets.

Interesting resources:
https://medium.com/better-programming/understanding-browser-networking-and-how-to-optimize-the-requests-for-http-1-1-and-http-2-f6371f0af650
https://medium.com/better-programming/10-extraordinary-github-repos-for-all-developers-939cdeb28ad0
