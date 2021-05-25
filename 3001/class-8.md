# API Design Best Practices

[API Design Best Practices](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)


## What does REST stand for?
an architectural approach to designing web services. REST is an architectural style for building distributed systems based on hypermedia. REST is independent of any underlying protocol and is not necessarily tied to HTTP


## REST APIs are designed around a 
2000.


## What is an identifer of a resource? Give an example.
A resource has an identifier, which is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:
https://adventure-works.com/orders/1


## What should the URIs be based on?
on nouns (the resource) and not verbs (the operations on the resource).

## Give an example of a good URI.
https://adventure-works.com/orders

## What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
an API may require a client application to send multiple requests to find all of the data that it requires.
we should avoide it(**bad**),because  all web requests impose a load on the web server. The more requests, the bigger the load.

## What status code does a successful GET request return?
 returns HTTP status code 200 (OK)

## What status code does an unsuccessful GET request return?
If the resource cannot be found, the method should return 404 (Not Found).

## What status code does a successful POST request return?
 it returns HTTP status code 201 (Created)

## What status code does a successful DELETE request return?
- A 202 (Accepted) status code if the action will likely succeed but has not yet been enacted.
- A 204 (No Content) status code if the action has been enacted and no further information is to be supplied.
- A 200 (OK) status code if the action has been enacted and the response message includes a representation describing the status.