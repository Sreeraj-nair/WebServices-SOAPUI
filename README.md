# WebServices-SOAPUI

### What is WebService?

 - Web Service allows a program to talk to an Engine/Server, instead of using your browser to open a web page. 
 
 - Unlike traditional client/server models, such as Web Server/Web Page system, web services do not provide the user with a GUI. 
 
 - Web Services instead share business logic, data and processes through a programmatic interface across a network. 
  
 - It is a service that allows communication between different applications developed using different programming languages. It allows 
 us to pass the data over the internet in easy way. 

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
We have two types of Web Services - 
1) SOAP Services 
- SOAP stands for Simple Object Access Protocol. SOAP itself is a protocol. 
- It is used to exchange between service and application in XML format. 
- SOAP is a wrapper over HTTP protocol, internally it uses HTTP protocol to transfer and receive XML messages. 
- SOAP uses Web Service Description Language (WSDL). 
- Standard, Heavy and Conventional. Heavy because we are sending so much of data to the server and receiving data back from the server. 
In XML we have to pass tags as well. 

Components of WSDL - 
* types: Describes datatype used by web service. 
* message: messages used by web services like zip code, address line 1 etc. 
* prototype: Operation performed by web service
* bindin: Communication protocols used in web service. 

2) REST Services
- REST is another way to develop web services. 
- REST users HTTP or other similar protocols. 
- It uses standard HTTP operations like GET, POST, PUT and DELETE. 
- New, light weighted, uses WADL (Web Application Description Language). 
- REST is a set of guidelines how a client should interact with server. 
- Resource: Data and functionality that a client can access from server is called a resource. 
- Each resource on server can be utilized by using its unique URI. 
- Response can be in format HTML, XML, plain text, JSON, PDF etc. 

### What is SOAP web services? 
- SOAP - stands for Simple Object Access Protocol
- SOAP can interact with other programming language applications. 
- It is just a protocol which is XML based for accessing web services over the internet. 
- It is recommended by W3C for communication between two applications over the network. 

Advantages of SOAP - 
-   1. SOAP has its own security known as WS Security. 
-   2. Language and platform independent. 
 
 Disadvantages of SOAP - 
-   1. It supports only XML format. 
-   2. It has many standards which we have to follow while working with SOAP UI so that's the reason it is slow. 
-   3. It works with WSDL File only so we can't use other formats like JSON, Header, Cookies and so on. 
  
### What is REST/Restful web services? 
- REST - stands for Representational State Transfer 
- It is platform independent. 
- It support multiple format like JSON, HTML, XML, Plain text file too. 
- It is fast as compared to SOAP. 
- It is not a protocol like SOAP, its just an architectural design. 

Rest Services are Light Weighted 
- Means less data transfer between client and server machine, ultimately need less bandwidth and fast. 
- In case of SOAP we can access complete application using WSDL. But in case of REST we can access only 1 functionality (Resource) by using URI. 
- REST uses main HTTP methods: 
* 1. GET to retreive resource
* 2. POST to create resource
* 3. PUT to update resource 
* 4. DELETE to Delete resource 

### Response Codes categories? 
- 1XX - Information based
- 2XX - Success 
- 3XX - Redirection 
- 4XX - Client error
- 5XX - Server error 

### What is WSDL or WSDL file? 
- 1. WSDL stands for Web Services Description language. 
- 2. WSDL is a language for describing web services and how to access them. 
- 3. WSDL is an XML format for describing services as a set of endpoints operating on messages containing either document-oriented 
or procedure-oriented information. 
- 4. The operations and messages are described abstractly, then bound to a concrete network protocol and message format to 
define an end point. 
- 5. Related concrete endpoints are combined into abstract endpoints (services). 

Eg. of WSDL - http://www.webservicex.com/CurrencyConvertor.asmx?wsdl 

### How to Create Project? 

### How to create a Test Case? 

### How to add a Test Step? 

### How to add Assertion? 

### How to define properties in SOAP UI? 
In SOAP UI we can define properties at four levels - 
- 1. Global Properties - Global properties can be used across all the projects within the workspace. 
  
     Syntax: ${globalTestData}
     
- 2. Project Level Properties - Project level properties can be used across all the test suites within the project. 

     Syntax: ${#Project#testProjectData}

- 3. Test Suite Level Properties - Test Suite level properties can be used across all the test cases within the suite. 

     Syntax: ${#TestSuite#testSuiteData}

- 4. Test Case Level Properties - Test Case level properties can be user across all the test steps within the test case. 
 
     Syntax: ${#TestCase#testCaseData}
