Resources from [The Odin Project](https://www.theodinproject.com/courses/web-development-101/lessons/how-does-the-web-work)

Resources that are useful and have stuff worth remembering


### 1. Short animated video on how the web works at a very big picture level
https://vimeo.com/128575085  
  
**Key words from the video**
1. Network -- connecting all the nests/nodes together with wires.
2. Protocols -- Predefined and agreed upon means of exchaning info or messages across the network. Can't just send some aribitrary signal over the network and have it be understood
3. Packets -- break up messages to send. has to and from info and instructions on how it fits together with other packets to make the actual message.
4. IP Addresses -- each nest has a unique address
5. DNS servers -- Giant address books for looking up the destination nest
6. Routers -- for moving packets across the network 

So you nodes and if you can find some way of connecting the nodes and passing meaningful information back and forth between the nodes, you have a network.

### 2. Short animated video on how search works at a very big picture level  
https://vimeo.com/128575084  
  
**Key words from the video**
1. Search engine -- Program for search
2. Web crawlers -- Search engines use these. Programs that go to the web and link from one page to the other and keep on doing that. They send a copy of each of the pages they've crawled through to the main search engine.
3. Index -- The engine builds an indes of words contained on each of the pages
4. Algorithms -- Applies algorithms to the index to find the best fitting and relevant results for your search
5. Relevant results ^^
6. Ranking -- Search engine ranks all relevant results so you've the highest quality results from search
7. Quality of web page -- how often updated, how well written, how well linked -- determines search ranking

### 3. One of the best one page guide to what the internet is and how it works from MDN    
https://developer.mozilla.org/en-US/docs/Learn/Common_questions/How_does_the_Internet_work#Summary  
  
Can't really do justice to the write up through a summary. The one page is a really summary of the internet and the web and provides a really good understanding and model for reasoning about the internet and the services built on top of it, of which the Web is an example.
  
1. Difference between router and modem?
   Router is just a computer albeit a special one just for routing packets between computers/servers connected to the router.
   Modem is a device that converts HTTP packets into packets that can be sent over phone lines/copper cables and does the opposite as well.
2. What is a router?
3. What is a modem?
4. Differentiate between the internet vs the Web.
5. In what way are Web, Email and IRC similar? (Services built on top of Internet.)
6. How do we keep track of all the computers connected to the internet?
7. What's a domain name?
  
Internet is simply a network of networks. And you can keep on scaling this and keeping on adding networks and keep on linking the networks. And run whatever service you want to over the network. Web, email, IRC, FTP or some other service. SSH is a protocol not a service. There's a SSH daemon or service on SSH servers to which SSH clients connect. 

Well, there is also a case for thinking of SSH as a service since you do have a SSH server on a remote machine that is always running and you can communicate with that using the SSH protocol.

Like even the Web, you have web apps running on web servers and you (the browser) can make requests to the web servers using the HTTP protocol.

So there's a one to one mapping between services/servers and protocols. You have different types of services running on servers and you can access these services with the associated protocols.

You can communicate with Web servers using the HTTP protocol.
With SSH servers using SSH protocol.
With FTP servers using the FTP protocol.
With email servers using the SMTP protocol.
And so on.

A fibre optic network like FIOS doesn't need to use a modem since copper cables are not being used. That's the reason why you only need a router to connect to FIOS. You don't need a modem to connect to FIOS. 

### 4. Explanation of client-server model of web from MDN    
https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works#Clients_and_servers  
  
Ok. Introduces the notion of protocols used for client/server communication between say a browser on a user computer and a sever serving google.com. 
TCP/IP stack and HTTP being the application protocol on top of the TCP/IP stack for enabling communication between the browser and the google server. And of course HTTP packets being sent back and forth during such communication and use of DNS lookup to find the server for google.com.

Worth rereading to lay down the mental model of how the protocols and data exchange between clients and servers happens.   

### 5.DNS from MDN. Pretty well written. Slightly differs in how it presents implementation when compared to the above video.
This seems to hide the details.  
https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_domain_name#How_does_a_DNS_request_work  

It does hide the details but accurately presents the high level steps in a DNS lookup. 

The most significant point here is that the DNS lookup starts with your computer. The browser is not directly communicating with a DNS server. The browser is asking your computer for the IP address and the computer then in turn is asking a DNS server for the IP address to provide to the browser. 

Don't know how the computer is communicating with a DNS server.
Fascinating. So, the computer is getting it's IP address and IP address of the DNS server to use from the DHCP server which is run on the router? Yes the router is being used as a DHCP server. Example: https://www.verizonwireless.com/support/knowledge-base-65774/. So the DHCP server in turn fetch it's IP address and the IP address of the DNS servers to use from the ISP's DHCP server. 
So you can change the settings of either your computer or your local DHCP server running on your router to use different DNS servers such as Open DNS or Google DNS. 

This is a good evolution and background of DNS: http://www.steves-internet-guide.com/dns-guide-beginners/
Some good answers on how a computer knows which DNS to use: https://www.quora.com/How-does-the-computer-know-which-DNS-server-to-use


### 5. One of the best intro books on HTTP    
https://launchschool.com/books/http


### 6.Difference b/w common terms. Ehh    
https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Pages_sites_servers_and_search_engines#Summary  
  
Worth a quick skim.

### 7. Entertaining and informative video on how DNS works  
https://www.youtube.com/watch?v=72snZctFFtA&feature=youtu.be&t=45s  


### 8.Ok guide to how the internet works without too much of the details, but the right model for understanding the web and internet    
https://www.youtube.com/watch?v=7_LPdttKXPc&feature=youtu.be&t=46s  
  
Redundant after the above resources
