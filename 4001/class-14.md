## Review, Research, and Discussion

### What’s the difference between a FIFO and a standard queue?
[ref](https://cloudaffaire.com/sqs-standard-vs-fifo-queue/)
A standard queue is used for application where the throughput of messages is more important than the ordering of messages while is used for application where the ordering of messages is more important than the throughput of the messages. 
### How can the server be assured a message was properly received?
[ref](https://stackoverflow.com/questions/36048164/message-queue-architecture-client-to-web-server-to-worker-and-back)
 the HTTP request handler sends the message across RabbitMQ and then sends an HTTP response back to the web browser.
### What classic design pattern is best represented by event driven programming?
[ref](https://levelup.gitconnected.com/understanding-event-driven-design-patterns-for-microservices-659b3c9fb51f)
Modelling and designing Event-Driven systems is challenging— both practically and conceptually. However, they promise scalability and performance at scales we haven’t seen before.
### How do you test an event driven system?
send emit and test the event
## Document the following Vocabulary

## Terms
### Term:


### FIFO Queue:
[ref](https://docs.aws.amazon.com/AWSSimpleQueueService/latest/SQSDeveloperGuide/FIFO-queues.html)
are designed to enhance messaging between applications when the order of operations and events is critical, or where duplicates can't be tolerated

### Pub/Sub:
[ref](https://aws.amazon.com/pub-sub-messaging/)
is a form of asynchronous service-to-service communication used in serverless and microservices architectures


## SNS vs SQS:
[ref](https://stackoverflow.com/questions/13681213/what-is-the-difference-between-amazon-sns-and-amazon-sqs)

#### SNS is a distributed publish-subscribe system. Messages are pushed to subscribers as and when they are sent by publishers to SNS.

#### SQS is distributed queuing system. Messages are not pushed to receivers. Receivers have to poll or pull messages from SQS


### Key Differences
[ref](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)
#### Entity Type
- SQS : Queue (similar to JMS, MSMQ).
- SNS : Topic-Subscriber (Pub/Sub system).
#### Message consumption
- SQS : Pull Mechanism — Consumers poll messages from SQS.
- SNS : Push Mechanism — SNS pushes messages to consumers.
#### Persistence
- SQS : Messages are persisted for some duration is no consumer available. The retention period value is from 1 minute to 14 days. The default is 4 days.
- SNS : No persistence. Whichever consumer is present at the time of message arrival, get the message and the message is deleted. If no consumers available then the message is lost.
In SQS the message delivery is guaranteed but in SNS it is not.
#### Consumer Type
- SQS : All the consumers are supposed to be identical and hence process the messages in exact same way.
- SNS : All the consumers are (supposed to be) processing the messages in different ways.
