## What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?
[ref](https://stackoverflow.com/questions/39356517/correct-way-to-pre-load-component-data-in-reactredux#:~:text=1%20Answer&text=The%20most%20'redux%2Dlike',Component%20that%20wraps%20your%20app.)
The most 'redux-like' way of handling the pre-loading of data would be to fire off the asynchronous action in the lifecycle method (probably componentWillMount ) of a Higher Order Component that wraps your app.



## When using a thunk/async action that dispatches the actual action, which do you export from your reducer?

 You export the async action and that will dispatch the response data to your action which will send the data to the reducer


## Term



### middleware
[ref](https://www.ibm.com/cloud/learn/middleware#:~:text=Middleware%20is%20software%20that%20enables,components%20in%20a%20distributed%20network.&text=There%20are%20many%20types%20of,on%20one%20type%20of%20communication.)
is software that enables one or more kinds of communication or connectivity between two or more applications or application components in a distributed network.


### thunk
[ref](https://github.com/reduxjs/redux-thunk)
A thunk is a function that wraps an expression to delay its evaluation.

```
// calculation of 1 + 2 is immediate
// x === 3
let x = 1 + 2;

// calculation of 1 + 2 is delayed
// foo can be called later to perform the calculation
// foo is a thunk!
let foo = () => 1 + 2;
```



### Redux Toolkit
[redux-toolkit](https://redux-toolkit.js.org/introduction/getting-started), []()
#### Redux Toolkit
Redux Toolkit is approach for writing Redux logic. It wraps around the Redux core, and contains packages and functions that we think are essential for building a Redux app. Redux Toolkit builds in our suggested best practices, simplifies most Redux tasks, prevents common mistakes, and makes it easier to write Redux applications.



#### Purpose
The Redux Toolkit package is intended to be the standard way to write Redux logic. It was originally created to help address three common concerns about Redux:

- "Configuring a Redux store is too complicated"
- "I have to add a lot of packages to get Redux to do anything useful"
- "Redux requires too much boilerplate code"


#### What's Included
Redux Toolkit includes these APIs:

- configureStore(): wraps createStore to provide simplified configuration options and good defaults. It can automatically combine your slice reducers, adds whatever Redux middleware you supply, includes redux-thunk by default, and enables use of the Redux DevTools Extension.
- createReducer(): that lets you supply a lookup table of action types to case reducer functions, rather than writing switch statements. In addition, it automatically uses the immer library to let you write simpler immutable updates with normal mutative code, like state.todos[3].completed = true.
- createAction(): generates an action creator function for the given action type string. The function itself has toString() defined, so that it can be used in place of the type constant.
- createSlice(): accepts an object of reducer functions, a slice name, and an initial state value, and automatically generates a slice reducer with corresponding action creators and action types.
- createAsyncThunk: accepts an action type string and a function that returns a promise, and generates a thunk that dispatches pending/fulfilled/rejected action types based on that promise
- createEntityAdapter: generates a set of reusable reducers and selectors to manage normalized data in the store
The createSelector utility from the Reselect library, re-exported for ease of use.


#### RTK Query 

RTK Query is provided as an optional addon within the @reduxjs/toolkit package. It is purpose-built to solve the use case of data fetching and caching, supplying a compact, but powerful toolset to define an API interface layer for your app. It is intended to simplify common cases for loading data in a web application, eliminating the need to hand-write data fetching & caching logic yourself.


#### What's included#
RTK Query includes these APIs:

- createApi(): The core of RTK Query's functionality. It allows you to define a set of endpoints describe how to retrieve data from a series of endpoints, including configuration of how to fetch and transform that data. In most cases, you should use this once per app, with "one API slice per base URL" as a rule of thumb.
- fetchBaseQuery(): A small wrapper around fetch that aims to simplify requests. Intended as the recommended baseQuery to be used in createApi for the majority of users.
- ApiProvider: Can be used as a Provider if you do not already have a Redux store.
- setupListeners(): A utility used to enable refetchOnMount and refetchOnReconnect behaviors.


#### HOOKState:
[hookstate](https://github.com/avkonst/hookstate)
Hookstate is a modern alternative to Redux, Mobx, Recoil, etc. It is simple to learn, easy to use, extendable, very flexible and capable to address all state management needs of large scalable applications. It has got impressive performance and predictable behavior.