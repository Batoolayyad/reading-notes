
### Describe the similarities between AWS API Gateway + Lambda functions and an ExpressJS Server
* Express apps are easy to build. 
* Lambda functions use an execution role to get permission to write logs to Amazon CloudWatch Logs, and to access other services and resources.
* Express is a minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications.
### List the AWS Database offerings and talk about the pros and cons of each
* **Relational** : Traditional applications, ERP, CRM, e-commerce
* **Key-value** : High-traffic web apps, e-commerce systems, gaming applications
* **In-memory** : Caching, session management, gaming leaderboards, geospatial applications
* **Document** : Content management, catalogs, user profiles
* **Wide Column** : High scale industrial apps for equipment maintenance, fleet management, and route optimization.
* **Graph** : Fraud detection, social networking, recommendation engines.
* **Time Series** : IoT applications, DevOps, industrial telemetry
* **Ledger** : Systems of record, supply chain, registrations, banking transactions.
### What's the difference between a FIFO and a standard queue?
FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing. FIFO queues provide additional features that help prevent unintentional duplicates from being sent by message producers or from being received by message consumers.
### How can the server be assured a message was properly received?
prepares a request with a certain attributes set and sends it to server.then getting an acknowledgement from the client
## Terms
##### Serverless API :
  Its is an API deployed by serverless service.
##### Triggers :
 Pieces of code that will automatically respond to any events in DynamoDB Streams. Triggers allow you to build applications that will then react to any data modification made in DynamoDB tables.
##### Dynamo vs Mongo :
  - MongoDB is vendor agnostic, Open Source, and can be deployed anywhere. DynamoDB is only available on AWS.
  - DynamoDB is a fully managed AWS service, MongoDB can be self installed or fully managed with MongoDB Atlas.
  - DynamoDB as an integrated AWS service makes it easier to develop end to end solutions.
  - DynamoDB uses tables, items and attributes, MongoDB uses JSON-like documents.
  - DynamoDB supports limited data types and smaller item sizes; MongoDB supports more data types and has fewer size restrictions.
##### Dynamoose vs Mongoose :
The most popular solutions for NoSQL databases are MongoDB and AWS DynamoDB. Both are widely used and offer highly scalable cloud-level service. Your organization's long-term cloud strategy and business-specific application requirements will be the key factor to determine which NoSQL database will work the best.


### SQS and SNS
[AWS SQS vs SNS](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)
* **SNS** is a distributed publish-subscribe service.
* **SQS** is distributed queuing service.


### SNS:
Amazon SNS is a fast, flexible, fully managed push notification service that lets you send individual messages or to bulk messages to large numbers of recipients. Amazon SNS makes it simple and cost effective to send push notifications to mobile device users, email recipients or even send messages to other distributed services.


### SQS:
is distributed queuing system. Messages are not pushed to receivers. Receivers have to poll SQS to receive messages. 


### Amazon SQS

Amazon SQS is a reliable, highly-scalable hosted queue for storing messages as they travel between applications or microservices. Amazon SQS moves data between distributed application components and helps you decouple these components.

For information on the permissions you need to use this API, see Identity and access management in the Amazon SQS Developer Guide.

You can use Amazon Web Services SDKs to access Amazon SQS using your favorite programming language. The SDKs perform tasks such as the following automatically:

Cryptographically sign your service requests

Retry requests

Handle error responses


