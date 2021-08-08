## Review, Research, and Discussion


### How does React differ from vanilla JS/HTML/CSS?
[ref](https://www.framer.com/blog/posts/react-vs-vanilla-js/)
- Plain JS apps usually start with the initial UI created on the server (as HTML), whereas React apps start with a blank HTML page, and dynamically create the initial state in JavaScript.

- React requires you to break your UI into components, but plain JS apps can be structured in any way you see fit.

- Data for plain JS apps are stored in the DOM itself and has to be found from the DOM before it can be used. React apps store data in regular JavaScript variables

- UI updates in plain JS have to happen by finding the DOM node to update and manually appending or removing elements. React automatically updates the UI based on setting and changing state within the component.



### What is the primary difference between a function component and a class component?
[ref](https://www.geeksforgeeks.org/differences-between-functional-components-and-class-components-in-react/)



- **functional component** is just a plain JavaScript function that accepts props as an argument and returns a React element.


**class component** requires you to extend from React. Component and create a render function which returns a React element.


- **functional component** use no render method, **class component** It must have the render() method returning HTML.

- React lifecycle methods (for example, componentDidMount) cannot be used in **functional components**. React lifecycle methods can be used inside **class components** (for example, componentDidMount).


## Term


### Functional Components
The first and recommended component type in React is functional components. A functional component is basically a JavaScript/ES6 function that returns a React element (JSX). 


### Children / Child Components
Child components are nested components that inherit props from their parent.

## hooks
[making sense of hooks](https://medium.com/@dan_abramov/making-sense-of-react-hooks-fdbde8803889)


## What Are Hooks?

Hooks let you use React features (like state) from a function — by doing a single function call without using class. React provides a few built-in Hooks exposing the “building blocks” of React: state, lifecycle, and context.

## Using the State Hook
[Using the State Hook](https://reactjs.org/docs/hooks-state.html)

#### What does calling useState do? It declares a “state variable”


#### What do we pass to useState as an argument? The only argument to the useState() Hook is the initial state.


#### What does useState return? It returns a pair of values: the current state and a function that updates it.


#### example to get familiar with Hooks:


```
import React, { useState } from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

### When would I use a Hook?
 If you write a function component and realize you need to add some state to it, previously you had to convert it to a class. Now you can use a Hook inside the existing function component. We’re going to do that right now!


## Hooks at a Glance

[Hooks at a Glance](https://reactjs.org/docs/hooks-overview.html)


### The Effect Hook
The Effect Hook, useEffect, adds the ability to perform side effects from a function component. It serves the same purpose as componentDidMount, componentDidUpdate, and componentWillUnmount in React classes, but unified into a single API.