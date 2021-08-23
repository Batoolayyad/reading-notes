## How granular should your reducers be?
[ref](https://sayefdeen.github.io/reading-notes401/class-38)
It depends, since we can separate the reducers for each component if we want to apply an action on that component i don’t think that we need to make general for all components


## Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched
[ref](https://sayefdeen.github.io/reading-notes401/class-38)

it is a Pro more than a Con since we have to change multiple states in multiple components, the fact that all the reducers can listen when the action is dispatched can reduce a lot of work, each reducer can provide a different logic to the same dispatcher.


## Name a strategy for preventing the above
[ref](https://sayefdeen.github.io/reading-notes401/class-38)

Make a reducer for each component that will be affected by the dispatcher, only effecting a specific amount of the state it self.


## Term


### store
[ref](https://redux.js.org/api/store)
A store holds the whole state tree of your application. The only way to change the state inside it is to dispatch an action on it.


### combined reducers
[ref](https://redux.js.org/api/combinereducers/)
The combineReducers helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.


## async actions
[async actions](https://redux.js.org/tutorials/fundamentals/part-6-async-logic)

### REST API and Client

The API uses /fakeApi as the base URL for the endpoints, and supports the typical GET/POST/PUT/DELETE HTTP methods for /fakeApi/todos. It's defined in src/api/server.js.

The project also includes a small HTTP API client object that exposes client.get() and client.post() methods, similar to popular HTTP libraries like axios. It's defined in src/api/client.js.

We'll use the client object to make HTTP calls to our in-memory fake REST API for this section.

### Redux Middleware and Side Effects

Redux store doesn't know anything about async logic. It only knows how to synchronously dispatch actions, update the state by calling the root reducer function, and notify the UI that something has changed. Any asynchronicity has to happen outside the store.
##### A "side effect" is any change to state or behavior that can be seen outside of returning a value from a function.


### Using Middleware to Enable Async Logic

Both of the middleware in that last section were very specific and only do one thing. It would be nice if we had a way to write any async logic ahead of time, separate from the middleware itself, and still have access to dispatch and getState so that we can interact with the store.


### Redux Async Data Flow

Just like with a normal action, we first need to handle a user event in the application, such as a click on a button. Then, we call dispatch(), and pass in something, whether it be a plain action object, a function, or some other value that a middleware can look for.


## Redux thunks:
[Redux thunks](https://github.com/reduxjs/redux-thunk)

### Why Do I Need This?

With a plain basic Redux store, you can only do simple synchronous updates by dispatching an action. Middleware extends the store's abilities, and lets you write async logic that interacts with the store.

Thunks are the recommended middleware for basic Redux side effects logic, including complex synchronous logic that needs access to the store, and simple async logic like AJAX requests.


### Motivation
Redux Thunk middleware allows you to write action creators that return a function instead of an action. The thunk can be used to delay the dispatch of an action, or to dispatch only if a certain condition is met. The inner function receives the store methods dispatch and getState as parameters.