# WebServices-SOAPUI

### What is WebService?
 - It is a service that allows communication between different applications developed using different programming languages. It allows 
 us 
to pass the data over the internet in easy way. 

- WebService provide an easy way to acheive interoperability. 

- It follows a collection of standards and protocols for exchaning information between two devices over the internet. 
Eg you are working on a banking application that requires data to be passed through multiple applications. 

- One application built using Java and other apps built using Python or Ruby. WebServices allows communication between such 
applications. 

Terminology - 
- Request: A request which is initiated by the client. 
- Response: An response send by the server based on client request. 

### Client Server Architecture? 
Consider the scenario. User opens a web browser. Types in https://www.google.com and hit enter button. A request is being sent by the 
client to the server. And in return server responds back with response code 200 OK. 

### What types of WebServies are supported by SOAPUI? 
Two - 
1) SOAP Services 
2) REST Services

### What is SOAP web services? 
SOAP - stands for Simple Object Access Protocol
SOAP can interact with other programming language applications. 
It is just a protocol which is XML based for accessing web services over the internet. 
It is recommended by W3C for communication between two applications over the network. 

Advantages of SOAP - 
  1. SOAP has its own security known as WS Security. 
  2. Language and platform independent. 
 
 Disadvantages of SOAP - 
  1. It supports only XML format. 
  2. It has many standards which we have to follow while working with SOAP UI so that's the reason it is slow. 
  3. It works with WSDL File only so we can't use other formats like JSON, Header, Cookies and so on. 
  
### What is REST/Restful web services? 
REST - stands for Representational State Transfer 
It is platform independent. 
It support multiple format like JSON, HTML, XML, Plain text file too. 
It is fast as compared to SOAP. 
It is not a protocol like SOAP, its just an architectural design. 

### Response Codes categories? 
1XX - Information based
2XX - Success 
3XX - Redirection 
4XX - Client error
5XX - Server error 

