## What’s the difference between PUT and PATCH?
[rapidapi](https://rapidapi.com/blog/put-vs-patch/)


PUT is a method of modifying resource where the client sends data that updates the entire resource. It is used to set an entity’s information completely. 
Unlike PUT, PATCH applies a partial update to the resource.
This means that you are only required to send the data that you want to update, and it won’t affect or change anything else. 


## Provide links to 3 services or tools that allow you to “mock” an API for development like json-server
[nordicapis](https://nordicapis.com/10-tools-to-mock-http-requests/)

1- Nock:an HTTPS library designed to replicate and mock servers and expectations in Node.js. Functionally, Nock does this by overriding both the http.request and http.

2- MockServer: is a multifaceted tool that comes in a variety of builds.

3- Beeceptor: is a great tool largely because it requires absolutely no code in order to utilize it


## Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?


apiDocjs: Inline Documentation for RESTful web APIs. It creates a documentation from API annotations in your source code. It includes a default template which uses handlebars, Bootstrap, RequireJS and jQuery for the output of the generated apidata.js and apiproject.js as a html-page; Swagger Inspector: Test and Document Your APIs With Ease. It is a free cloud-based API testing and documentation tool to simplify the validation of any API and generate its corresponding OpenAPI documentation. apiDocjs and Swagger Inspector can be primarily classified as "API" tools.


## Compare and contrast SOAP and ReST
[upwork](https://www.upwork.com/resources/soap-vs-rest-a-look-at-two-different-api-styles?utm_source=google&utm_campaign=SEM_GGL_INTL_NonBrand_Marketplace_DSA&utm_medium=cpc&utm_content=113089129402&utm_term=&campaignid=11384804789&matchtype=b&device=c&gclid=EAIaIQobChMI7uXLrdu48QIV1fhRCh29ZwpwEAAYASAAEgKdVvD_BwE)


**REST (Representational State Transfer)** is truly a “web services” API. REST APIs are based on URIs (Uniform Resource Identifier, of which a URL is a specific type) and the HTTP protocol, and use JSON for a data format, which is super browser-compatible. (It could also theoretically use the SOAP protocol, as we mentioned above.) REST APIs can be simple to build and scale, but they can also be massive and complicated—it’s all in how they’re built, added on to, and what they’re designed to do.


**SOAP (Simple Object Access Protocol)** is its own protocol, and is a bit more complex by defining more standards than REST—things like security and how messages are sent. These built-in standards do carry a bit more overhead, but can be a deciding factor for organizations that require more comprehensive features in the way of security, transactions, and ACID (Atomicity, Consistency, Isolation, Durability) compliance. For the sake of this comparison, we should point out that many of the reasons SOAP is a good choice rarely apply to web services scenarios, which make it more ideal for enterprise-type situations.


## Document the following Vocabulary Terms
### Web Server
A web server is a computer that runs websites. It's a computer program that distributes web pages as they are requisitioned. The basic objective of the web server is to store, process and deliver web pages to the users.


### Express
 is a minimal and flexible Node.js web application framework that provides a robust set of features to develop web and mobile applications. It facilitates the rapid development of Node based Web applications. Following are some of the core features of Express framework.


### routing
[cloudflare](https://www.cloudflare.com/learning/network-layer/what-is-routing/)
 Network routing is the process of selecting a path across one or more networks. In packet-switching networks, such as the Internet, routing selects the paths for Internet Protocol (IP) packets to travel from their origin to their destination. These Internet routing decisions are made by specialized pieces of network hardware called routers.


### WRRC
web request/response cycle 