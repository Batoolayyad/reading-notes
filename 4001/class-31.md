## Describe use cases useState() vs useReducer()
[ref](https://medium.com/@kavishkafernando/react-reducer-7dc653861c7a)
useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one.



## Why do custom hooks need the use prefix?
[ref](https://betterprogramming.pub/quick-intro-to-react-hooks-6e8a44ae4aa6)
Custom hooks are normal JS functions, named with the prefix 'use', that can use hooks inside of it and contain a common stateful logic to be reused in other components.



## What do custom hooks usually do?
[ref](https://www.wix.engineering/post/custom-react-hook-when-software-design-meets-react-hooks#:~:text=Custom%20hooks%20allow%20us%20to,use%20cases%20to%20reusable%20hooks.)
Custom hooks allow us to have cleaner functional components, remove logic from the UI layer, and prevent code duplication by bringing common use cases to reusable hooks.


## Using any list of custom hooks, research and name one that you think will be useful in your applications
[ref](https://usehooks.com/useScript/)
useScript React hook to dynamically load an external script and know when its loaded


## Describe how a hook that fetches API data might work
The hook might take in a url, a method, and a body. Using axios or something similar, useState and possibly useEffect, an API call can be made based on and using the parameters passed in and then an objects state could be ‘set’ based on the results of the API call.



## Term


### reducer:
The concept of a Reducer became popular in JavaScript with the rise of Redux as state management solution for React. Basically reducers are there to manage state in an application. For instance, if a user writes something in an HTML input field, the application has to manage this UI state (e.g. controlled components)


## Context
[ref](https://reactjs.org/docs/context.html)

Context provides a way to pass data through the component tree without having to pass props down manually at every level.

### When to Use Context?
Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language.


### Snackbars in React: An Exercise in Hooks and Context?
[ref](https://medium.com/swlh/snackbars-in-react-an-exercise-in-hooks-and-context-299b43fd2a2b)

Necessity for the Design System
After performing an audit on how we communicate with our users, we landed with a simple system of three classes of communication, and snackbars fit perfectly on the ‘low priority’ end of that spectrum. They are small notifications that show up on the screen when a user performs an action. They are not intrusive at all and appear for just a brief moment.



