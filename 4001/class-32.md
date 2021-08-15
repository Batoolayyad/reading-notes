## When you have multiple contexts, what component type should you use (class/function) and why?
function, If two or more context values are often used together, you might want to consider creating your own render prop component that provides both. 



## What are some good use cases for using the Context API for global state?
[ref](https://content.breatheco.de/en/lesson/context-api)
1- Centralizing a global application state: Instead of being limited to local states on views, you can now share data on one central component and spread to its inner components (children, grandchildren and so forth). The centralized state is called store and we can spread it by using the Context.Provider and Context.Consumer
2- Data propagation and re-rendering: when this centralized global state (store) changes, it triggers a re-render of all of the children compoments (your entire application) which produces new data to show up in the UI. A central setState*ish*.
3- If you've already worked with react, you've probably felt the frustration of passing properties throughout your application, we call it "property hell".


## How can you best test context?
[ref](https://www.samdawson.dev/article/react-context-testing)
The best way to test Context is to make our tests unaware of its existence and avoiding mocks. We want to test our components in the same way that developers would use them (behavioral testing) and mimic the way they would run in our applications (integration testing).

## Term


### context
Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language. 


### useContext()
[ref](https://reactjs.org/docs/hooks-reference.html#usecontext)
A component calling useContext will always re-render when the context value changes. If re-rendering the component is expensive


### static context
Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language. 


## Api

### React.createContext
```
const MyContext = React.createContext(defaultValue);
```

Creates a Context object. When React renders a component that subscribes to this Context object it will read the current context value from the closest matching Provider above it in the tree.

The defaultValue argument is only used when a component does not have a matching Provider above it in the tree. This default value can be helpful for testing components in isolation without wrapping them. Note: passing undefined as a Provider value does not cause consuming components to use defaultValue.

### Context.Provider

```
<MyContext.Provider value={/* some value */}>
```

All consumers that are descendants of a Provider will re-render whenever the Provider’s value prop changes. The propagation from Provider to its descendant consumers (including .contextType and useContext) is not subject to the shouldComponentUpdate method, so the consumer is updated even when an ancestor component skips an update.

Changes are determined by comparing the new and old values using the same algorithm as Object.is.


### Context.Consumer

```
<MyContext.Consumer>
  {value => /* render something based on the context value */}
</MyContext.Consumer>
```

A React component that subscribes to context changes. Using this component lets you subscribe to a context within a function component.

Requires a function as a child. The function receives the current context value and returns a React node. The value argument passed to the function will be equal to the value prop of the closest Provider for this context above in the tree. If there is no Provider for this context above, the value argument will be equal to the defaultValue that was passed to createContext().


### hooks and context example
After performing an audit on how we communicate with our users, we landed with a simple system of three classes of communication, and snackbars fit perfectly on the ‘low priority’ end of that spectrum. They are small notifications that show up on the screen when a user performs an action. They are not intrusive at all and appear for just a brief moment.

