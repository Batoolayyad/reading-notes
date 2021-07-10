## Why is access control important?
[the-important-of-access-control](https://premieritsolution.co.uk/the-important-of-access-control/)
Access control is important because it is a valuable security technique that can be used to regulate who or what can view or use any given resource.

## Describe an application that would need access control.
[application-areas-access-control-system](https://www.magnum.org.in/blog/application-areas-access-control-system/)
- For any organization in any field of activity: Restriction of access to office premises;
Control the movement of employees across the building; Automatic accounting of working hours;
- Healthcare: Restriction of access to office premises, including storage of particular drugs;
Control of obtaining medicines on a fingerprint;
- Financial institutions: Biometric ATM;
Biometric safes, postal and depository cells; The location and movement of employees and visitors;
- Educational institutions: Restriction of access to an educational institution; Informing parents about the student’s arrival and departure to the educational institution via SMS;


## What is a role used for?
[role-based-access-control-rbac](https://www.imperva.com/learn/data-security/role-based-access-control-rbac/)
involves setting permissions and privileges **to enable access to authorized users**



## Term


### Authorization

function of specifying access rights/privileges to resources


### Role Based Access Control
[role-based-access-control-rbac](https://www.imperva.com/learn/data-security/role-based-access-control-rbac/)
is a mechanism that restricts system access. It involves setting permissions and privileges to enable access to authorized users.


### Capabilities
[Roles, capabilities, and rights](http://publib.boulder.ibm.com/tividd/td/ITIM/SC32-0825-00/en_US/HTML/id21am09.htm#HDRID21AD0031012852)
Identifies one or more collections of rights. Capabilities provide a range of actions necessary to act on resources.




## Event-Driven Programming in Node.js
[Event-Driven Programming in Node.js](https://www.digitalocean.com/community/tutorials/nodejs-event-driven-programming)


### what is Event-Driven Programming?
is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision.

### Event-Driven Programming makes use of the following concepts:
* An Event Handler is a callback function that will be called when an event is triggered.
* A Main Loop listens for event triggers and calls the associated event handler for that event.

### what is EventEmitter?
module that is provided by Node.js natively, allows us to get started incorporating Event-Driven Programming in our project right away.

We access the EventEmitter class through the events module. Once imported we’ll need to create a new object from the class to start using it.

```
const EventEmitter = require('events').EventEmitter;
const myEventEmitter = new EventEmitter;

```

### how to remove Removing Listeners?

To remove event listeners in EventEmitter we can use the removeListener or removeAllListeners method.



