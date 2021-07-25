## Describe “The Cloud”
[ref](https://www.cloudflare.com/learning/cloud/what-is-the-cloud/)
refers to servers that are accessed over the Internet, and the software and databases that run on those servers. Cloud servers are located in data centers all over the world. By using cloud computing, users and companies don't have to manage physical servers themselves or run software applications on their own machines.


## What is a container (as it relates to computers and servers)?
[ref](https://www.docker.com/resources/what-container)
A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another




## What is auto-scaling?
[ref](https://aws.amazon.com/autoscaling/)
AWS Auto Scaling monitors your applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost.




## What is bandwidth?
[ref](https://en.wikipedia.org/wiki/Bandwidth_(computing))
bandwidth is the maximum rate of data transfer across a given path. 



## How do cloud providers compute service costs?
[ref](https://expedient.com/knowledgebase/blog/2015-05-01-how-the-cost-of-cloud-computing-is-calculated/)
When setting price, cloud providers determine the expense to maintaining the network. They start by calculating costs for network hardware, network infrastructure maintenance, and labor. These expenses are added together and then divided by the number of rack units a business will need for its IaaS cloud


## Term


### Server Instances
[ref](https://www.techopedia.com/definition/32149/server-instance#:~:text=A%20server%20instance%20is%20a,based%20or%20command%2Dline%20based.)
A server instance is a collection of SQL Server databases which are run by a solitary SQL Server service or instance. The details of each server instance can be viewed on the service console which can be web-based or command-line based.

### Containers
[ref](https://www.docker.com/resources/what-container)
A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another



### Cloud Services
[ref](https://www.akamai.com/us/en/resources/cloud-services.jsp#:~:text=Cloud%20services%20are%20services%20available,or%20networking%20via%20the%20internet.)
Cloud services are services available via a remote cloud computing server rather than an on-site server. These scalable solutions are managed by a third party and provide users with access to computing services such as analytics or networking via the internet.


### Cloud Architecture
[ref](https://en.wikipedia.org/wiki/Cloud_computing_architecture)
refers to the components and subcomponents required for cloud computing. These components typically consist of a front end platform (fat client, thin client, mobile ),back end platforms (servers, storage), a cloud based delivery, and a network (Internet, Intranet, Intercloud). Combined, these components make up cloud computing architecture.

### AWS
[ref](https://searchaws.techtarget.com/definition/Amazon-Web-Services)
AWS (Amazon Web Services) is a comprehensive, evolving cloud computing platform provided by Amazon that includes a mixture of infrastructure as a service (IaaS), platform as a service (PaaS) and packaged software as a service (SaaS) offerings


### EC2/Beanstalk vs Heroku

Heroku and AWS Elastic Beanstalk, solutions (production configurations) is that they have comparable features and pricing. One big difference is that Heroku’s pricing takes exponential price jumps as one adds common additional features, e.g., auto-scaling, where-as AWS pricing is fairly linear. On the other hand, Heroku is generally simpler to get up and running as AWS has a fairly steep initial learning curve.


## what is Amazon S3?
[AWS S3](https://aws.amazon.com/s3/)
Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance


## what is AWS Lambda?
- [AWS Lambda Basics](https://www.serverless.com/aws-lambda)
AWS Lambda is  serverless computing services.



- [AWS Lambda Functions](https://aws.amazon.com/lambda/)
 is a serverless compute service that lets you run code without provisioning or managing servers, creating workload-aware cluster scaling logic, maintaining event integrations, or managing runtimes.


## How does AWS Lambda work?
[AWS Lambda Basics](https://www.serverless.com/aws-lambda)
Each Lambda function runs in its own container. When a function is created, Lambda packages it into a new container and then executes that container on a multi-tenant cluster of machines managed by AWS. Before the functions start running, each function’s container is allocated its necessary RAM and CPU capacity. Once the functions finish running, the RAM allocated at the beginning is multiplied by the amount of time the function spent running. The customers then get charged based on the allocated memory and the amount of run time the function took to complete.


## What are the most common use cases for AWS Lambda?
[AWS Lambda Basics](https://www.serverless.com/aws-lambda)
1- individual tasks run for a short time;
2- each task is generally self-contained;
3- there is a large difference between the lowest and highest levels in the workload of the application.


## what (CDN)?
[CDN](https://cyberhoot.com/cybrary/content-delivery-network-cdn/)
Content Delivery Network (CDN) is a geographically distributed group of servers that work together to provide fast delivery of Internet content. 