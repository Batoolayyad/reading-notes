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


## inheritance
[MDN inheritance](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)


### what does prototype chain means and what the is the object structor?


JavaScript only has one construct: objects.Each object has a private property which holds a link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. By definition, null has no prototype, and acts as the final link in the prototype chain.

#### EXAPLE:

```
// Let's create an object o from function f with its own properties a and b:
let f = function () {
   this.a = 1;
   this.b = 2;
}
let o = new f(); // {a: 1, b: 2}

// add properties in f function's prototype
f.prototype.b = 3;
f.prototype.c = 4;

// do not set the prototype f.prototype = {b:3,c:4}; this will break the prototype chain
// o.[[Prototype]] has properties b and c.
// o.[[Prototype]].[[Prototype]] is Object.prototype.
// Finally, o.[[Prototype]].[[Prototype]].[[Prototype]] is null.
// This is the end of the prototype chain, as null,
// by definition, has no [[Prototype]].
// Thus, the full prototype chain looks like:
// {a: 1, b: 2} ---> {b: 3, c: 4} ---> Object.prototype ---> null

console.log(o.a); // 1
// Is there an 'a' own property on o? Yes, and its value is 1.

console.log(o.b); // 2
// Is there a 'b' own property on o? Yes, and its value is 2.
// The prototype also has a 'b' property, but it's not visited.
// This is called Property Shadowing

console.log(o.c); // 4
// Is there a 'c' own property on o? No, check its prototype.
// Is there a 'c' own property on o.[[Prototype]]? Yes, its value is 4.

console.log(o.d); // undefined
// Is there a 'd' own property on o? No, check its prototype.
// Is there a 'd' own property on o.[[Prototype]]? No, check its prototype.
// o.[[Prototype]].[[Prototype]] is Object.prototype and there is no 'd' property by default, check its prototype.
// o.[[Prototype]].[[Prototype]].[[Prototype]] is null, stop searching,
// no property found, return undefined.

```


### HOW to creat an object?
there are Different ways to create objects and the resulting prototype chain:


- Objects created with syntax constructs


```
var o = {a: 1};

// The newly created object o has Object.prototype as its [[Prototype]]
// o has no own property named 'hasOwnProperty'
// hasOwnProperty is an own property of Object.prototype.
// So o inherits hasOwnProperty from Object.prototype
// Object.prototype has null as its prototype.
// o ---> Object.prototype ---> null

var b = ['yo', 'whadup', '?'];

// Arrays inherit from Array.prototype
// (which has methods indexOf, forEach, etc.)
// The prototype chain looks like:
// b ---> Array.prototype ---> Object.prototype ---> null

function f() {
  return 2;
}

// Functions inherit from Function.prototype
// (which has methods call, bind, etc.)
// f ---> Function.prototype ---> Object.prototype ---> null
```


- With a constructor


A "constructor" in JavaScript is "just" a function that happens to be called with the new operator.


```
function Graph() {
  this.vertices = [];
  this.edges = [];
}

Graph.prototype = {
  addVertex: function(v) {
    this.vertices.push(v);
  }
};

var g = new Graph();
// g is an object with own properties 'vertices' and 'edges'.
// g.[[Prototype]] is the value of Graph.prototype when new Graph() is executed.
```


- With Object.create


```
var a = {a: 1};
// a ---> Object.prototype ---> null

var b = Object.create(a);
// b ---> a ---> Object.prototype ---> null
console.log(b.a); // 1 (inherited)

var c = Object.create(b);
// c ---> b ---> a ---> Object.prototype ---> null

var d = Object.create(null);
// d ---> null
console.log(d.hasOwnProperty);
// undefined, because d doesn't inherit from Object.prototype

```


- With the class keyword


## this :
[MDN this](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/this)


In most cases, the value of this is determined by how a function is called (runtime binding). It can't be set by assignment during execution, and it may be different each time the function is called.

### what is the value of this in each case of the following cases:

- **In the global execution context** (outside of any function), this refers to the **window object**


- **function context** Inside a function, the value of this depends on how the function is called.


- **Class context** Within a class constructor, this is a regular object. All non-static methods within the class are added to the prototype of this:


```
class Example {
  constructor() {
    const proto = Object.getPrototypeOf(this);
    console.log(Object.getOwnPropertyNames(proto));
  }
  first(){}
  second(){}
  static third(){}
}

new Example(); // ['constructor', 'first', 'second']
```


## Classes
[MDN classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)


### what does classe mean?

Classes are a **template for creating objects**. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics. 
 