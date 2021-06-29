## Name 3 real world use cases where you’d want to change the request with custom middleware
[selvaganesh93.medium.com](https://selvaganesh93.medium.com/how-node-js-middleware-works-d8e02a936113)
[digitalthinkerhelp](https://digitalthinkerhelp.com/what-is-middleware-architecture-types-examples-applications/)

1- Auth middleware
2-Game Engines
3-Integration Middleware


## True or false: The route handler is middleware?
[selvaganesh93.medium.com](https://selvaganesh93.medium.com/how-node-js-middleware-works-d8e02a936113)


A middleware is basically a function that will the receive the Request and Response objects, just like your route Handlers do, but the different is that as a third argument middleware has next which is a function you should call once your middleware code completed.


## In what ways can a middleware function end the process and send data to the browser?


By using next()


## At what point in the request lifecycle can you “inject” middleware?
[stackoverflow](https://stackoverflow.com/questions/13690840/can-you-insert-middleware-in-an-node-js-express-app)


you can pass your app object to other modules and call use there. Of course, middleware functions are executed in the order they are added, so you have to take great care to ensure that you call use in the correct order.
As far as actually injecting a middleware function in the middle of the stack (after you've already called app.use with a set of middleware functions), there's no documented way to do it. use only adds a function to the end of the stack.


## What can cause express to error with “Request headers sent twice, cannot start a second response”


sending more then one request and geting many responses at one time.


## Document the following Vocabulary Terms


### Middleware
[expressjs](https://expressjs.com/en/guide/using-middleware.html)


 functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. The next middleware function is commonly denoted by a variable named next


### Request Object
[expressjs](https://expressjs.com/en/guide/using-middleware.html)


The req object represents the HTTP request and has properties for the request query string, parameters, body, HTTP headers, and so on. In this documentation and by convention, the object is always referred to as req (and the HTTP response is res) but its actual name is determined by the parameters to the callback function in which you’re working.

For example:
```
app.get('/user/:id', function (req, res) {
  res.send('user ' + req.params.id)
})
```


### Response Object
[expressjs](https://expressjs.com/en/guide/using-middleware.html)


The res object represents the HTTP response that an Express app sends when it gets an HTTP request.
In this documentation and by convention, the object is always referred to as res (and the HTTP request is req) but its actual name is determined by the parameters to the callback function in which you’re working.
For example:
```
app.get('/user/:id', function (req, res) {
  res.send('user ' + req.params.id)
})
```


### Application Middleware

Bind application-level middleware to an instance of the app object by using the app.use() and app.METHOD() functions, where METHOD is the HTTP method of the request that the middleware function handles (such as GET, PUT, or POST) in lowercase.


### Routing Middleware
[trycoder](https://www.trycoder.com/2021/02/express-router-level-middleware.html)


 a middleware used in creating routes. Though there’s another alternative to creating a route in a node js app, there are cases where a middleware for a particular functionality is very necessary especially medium-large apps. Also, the router middleware is used to group the routes of a website together and access them easily.


### Test Driven Development(TDD)
[bmc](https://www.bmc.com/blogs/testing-frameworks-unit-functional-tdd-bdd/)


 is a clever idea to get programmers to focus on just what is important and not get stuck in the time-consuming task of solving esoteric problems or those that are not germane to the main task. TDD is an extension of the Agile Framework, whose goal is speed through simplicity and simplicity by delivering small discrete tasks and tracking those instead of trying to write an entire application per some giant GANTT chart, a process that is usually doomed to failure, say the Agile advocates.

### Behavioral Testing
[bmc](https://www.bmc.com/blogs/testing-frameworks-unit-functional-tdd-bdd/)


 is based on the same idea as TDD, but its focus is on the application and not testing individual paragraphs of code. So it is automated functional testing.


 ## Review: ES6 Classes
 [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

 #### what Classes mean?
 Classes are a template for creating objects. They encapsulate data with code to work on that data.

 #### what ES6 Classes?
 Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class-like semantics.

 #### give an Example on ES6 Classes:

 ```
 class Rectangle {
  constructor(height, width) {
    this.height = height; 
    this.width = width;
  }
}
```
#### what is the parts for classes?


- body: is the part that is in curly brackets {}. This is where you define class members, such as methods or constructor.

- constructor: is a special method for creating and initializing an object created with a class. There can only be one special method with the name "constructor" in a class.

- Static properties and methods: Static members (properties and methods) are called without instantiating their class and cannot be called through a class instance. Static methods are often used to create utility functions for an application, whereas static properties are useful for caches, fixed-configuration, or any other data you don't need to be replicated across instances.


## Using Express Routing
[expressjs](https://expressjs.com/en/guide/routing.html)


#### What does Routing mean?


Routing refers to how an application’s endpoints (URIs) respond to client requests.
and it is defined by using methods of the Express app object that correspond to HTTP methods.


#### How we get the Route methods?

A route method is derived from one of the HTTP methods(GET,POST,PUT,DELETE), and is attached to an instance of the express class.
example:

```
// GET method route
app.get('/', function (req, res) {
  res.send('GET request to the homepage')
})
```

#### what does Route paths mean?

define the endpoints at which requests can be made. Route paths can be strings, string patterns, or regular expressions.


## Express Routing
[scotch.io](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)


#### What exactly is the Express Router?


Router is like a mini express application. It doesn't bring in views or settings, but provides us with the routing APIs like .use, .get, .param, and route.

#### we can create multiple express.Router()s and then apply them to our application. We could have a Router for our basic routes, authenticated routes, and even API routes.

#### Using the Router allow us to make applications more modular and flexible by creating multiple instances of the Router and applying them accordingly. 



