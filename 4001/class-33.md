
## Why is the Context API useful?
a way for a React app to effectively produce global variables that can be passed around. This is the alternative to “prop drilling” or moving props from grandparent to child to parent. Also context is also touted as an easier, lighter approach to state management using Redux.


## Can a component outside of a provider get its context?
cannot get Context.Provider.


## What are some common use cases for using the Context API?
Useful for sharing data that can be considered global, such as currently authenticated user, or theme settings for the application.




## Describe “Context Hell”
Context API has virtually no boilerplate in comparison to Redux, adding Context Providers makes for messy and unreadable code.





## Term


### global state
Context API has virtually no boilerplate in comparison to Redux, adding Context Providers makes for messy and unreadable code.




### global context
This is context that affects the entire application, and it will share data to everything in the React component tree.



### provider
makes the Redux store available to any nested components that need to access the Redux store


### consumer
This is a React component that subscribes to context changes in value of the Provider.



### DEFINITION OF ROLE-BASED ACCESS CONTROL (RBAC)
Role-based access control (RBAC) restricts network access based on a person's role within an organization and has become one of the main methods for advanced access control. The roles in RBAC refer to the levels of access that employees have to the network.

### BENEFITS OF RBAC
Managing and auditing network access is essential to information security. Access can and should be granted on a need-to-know basis



### react-cookies:
Cookies are the data stored in the form of key-value pairs that are used to store information about the user on their computer by the websites that the users browse and use it to verify them. To set or remove the cookies, we are going to use a third-party dependency of react-cookie.



