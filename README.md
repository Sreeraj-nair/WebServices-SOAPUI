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

SOAP defines W3C standards to be strictly followed, which takes more time to develop, test and use. 
REST doesn't define too much standards like SOAP. 

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
- Right click on the Workspace and click New SOAP project. 
- Click on OK. 
- Provide WSDL path and type Project Name. 
- SOAPUI scans the WSDL file and all the services provided by this WSDL is listed in the tool. 
- Eg GetCountries service provides all the countries in the word. 
- Create a Test Suite within the Project. 

### How to create a Test Case? 
- Create a Test Case. 
- Right click on test case, click SOAP Test Request. 
- Input test case name. 
- Select a service you want to use in the service. 

### How to add a Test Step? 
- A new test step gets created in the test case. 

### How to add Assertion? 
- Can use contains, not contains, xpath, xquery so on for validating the response. 

### How to define properties in SOAP UI? 
In SOAP UI we can define properties at four levels. They are also known as variables. 
- 1. Global Properties - Global properties can be used across all the projects within the workspace. 
Go to File > Preferences. Global Properties can be define here. 
  
     Syntax: ${globalTestData}
     
- 2. Project Level Properties - Project level properties can be used across all the test suites within the project. 
Double click on Project Name > On the properties tab, click + to create a new property. 

     Syntax: ${#Project#testProjectData}

- 3. Test Suite Level Properties - Test Suite level properties can be used across all the test cases within the suite. 
Double click on Test Suite Name > On the properties tab, click + to create a new property. 

     Syntax: ${#TestSuite#testSuiteData}

- 4. Test Case Level Properties - Test Case level properties can be user across all the test steps within the test case. 
Double click on Test Case Name > On the properties tab, click + to create a new property. 
 
     Syntax: ${#TestCase#testCaseData}

- 5. We can also create propeties inside the test case as well. 
Right Click on Test Step > Click on Properties. 

     Syntax: ${#Properties#testStepData}

### What is a Manual test step? 
Create a project within the workspace. Create test suite, test case and Step1 to the test case. Right click and add Step2. 
Now if you want to add a delay test step. Add a test step Delay 100000 MS = 100 seconds. In this 100 seconds can go to 
the server and restart it. Pause of 100 seconds. 
In this case we can add a Manual Test Step, if the server is not getting started. This can be used to perform manual tasks by adding. 
In the description field mention the task. Expected result is server should be started successfully. 
When a test runs, a pop up will come up and expect user to enter the acual result and pass/fail the test. 

### What is a Data Source and Data Sink in SoapUI PRO? 
- Create a new SOAP project using WSDL. Provide name DataSource. 
- Scanning the WSDL and populate the operations. 
- Inside the suite, create case1, inside the case create Step1_Add. 
- Add DataSource and place it at the start. Create value1 and value2.
- Create an excel file with value1 and value2 in A and B columns of excel file. 
- Name the file as Input.xls, save it. 
- Provide the location of the xls in the File path. 
- Provide worksheet name - Sheet1
- Provide first column name, Sheet at Cell - A1
- Run the step, all the data from the excel will be populated. 
- Go to test step and provide references to Data Source - value1 and value2 for test data.
- To execute the test in loop, we need to add DataSource Loop. Starting with Step1_Add and end with DataSource Loop. 
- For storing the results in File, add another step called DataSink. Provide the file path. 
- Run the tests, execute successfully, we need to notice only one result is getting saved. 
- Mode DataSourceLoop to the end of the Steps. 

### Parameterization and Data Driven Testing in SOAPUI PRO
- We have a Project > Test Suite > Test Case > Test Steps in SOAP UI. 
- Add SOAP Test Request - Req1 GetCountryByCountryCode.
- Check if server is working with single data. 
- Create a xlsx file. In first column provide countryCode and in second column countryName. Save a Excel Workbook named SoapTestData.xlsx  
- Move to SOAP UI Pro. 
- Add a TestStep DataSource with Properties Code and Country - Provide file path. 
- Provide Sheet name - Sheet1
- Provide starting point - A1. 
- Execute the step to check by entering 0 to pick all data from excel file. 
- Best practive put DataSource at the top. 
- Define the loop to run with multiple data. 
- Add DataSource Loop Test step. Dounble click and define the data source step (defines number of time loop to run) and Target Step is starting point of the loop i.e. Req1. 
- Add a Delay step in between. 
- End point is always DataSource Loop. 

### XPath Assertion in SOAP UI Free version
- Create a Project > Test Suite > Test Case > Test Step > SOAP Test Request > Step1_GetCityForcastByZIP. 
- Let's see how we make Xpath assertion. 
- Go to TestStep. 
- Click on Assertion tab, click on + button. 
- On Property Content bar, select XPath Match. XPath Match Configuration window pops up. By default it is empty. 
- First we need to set the namespace. For that clare Declare button. SOAP UI will store the url in the name space. 
  
   declare namespace soap='http://schemas.xmlsoap.org/soap/envelope';
   declasre namespace ns1='http://ws.cdyne.com/WeatherWS/';
   
- Start typing //ns1:GetCityForecastByZIPResponse/ns1:GetCityForecastByZIPResult/ns1:City
- Click Select from current. 
- Will fetch New York. 
- Start typing //ns1:GetCityForecastByZIPResponse/ns1:GetCityForecastByZIPResult/ns1:ForecastResult
This will return all the results. 





