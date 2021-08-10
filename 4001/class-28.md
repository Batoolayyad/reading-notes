## Review, Research, and Discussion


### Why do we not need more .html pages in a multi-page React app?
[ref](https://morioh.com/p/1e31a980e5a6)
In Multi-page apps, we get back multiple HTML pages, where each page has content for given Router.

### If we wanted a component to show up on every page, where would we put it and why?
[react-router-cheatsheet](https://www.freecodecamp.org/news/react-router-cheatsheet/)


Inside the **BrowserRouter**, outside a **Route**, because all the components need to be inside the Browser Router but if we have it inside the Route it will have specific path to display it.


### What does routing do with the components that were rendered when a new route is requested?
render the component for the new route that is requested 


### What does props.children contain?
[ref](https://codeburst.io/a-quick-intro-to-reacts-props-children-cb3d2fce4891) React docs say that you can use props.children on components that represent ‘generic boxes’ and that ‘don’t know their children ahead of time’.
simple explanation of what this.props.children does is that it is used to display whatever you include between the opening and closing tags when invoking a component.


### How do useState() and this.setState() differ?
[ref](https://www.reddit.com/r/reactjs/comments/b46fv0/the_difference_between_setstate_and_usestate/)

setState is merging the previous state with the new one, it means that you dont have to pass the full state object every time you want to change some part of the state. React will update given properties and won't touch the rest. The useState's updater rewrites a previous state with a new one and it does not perform any merging. Its just replacement instead of merging.



## Term


### State Hook
[hooks-state](https://reactjs.org/docs/hooks-state.html)
A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components. We’ll learn other Hooks later.



### Mounting and Un-Mounting
[ref](https://learn.co/lessons/react-component-mounting-and-unmounting)
A React component's lifecycle contains distinct phases for creation and deletion. In coding terms, these are called mounting and unmounting. You can also think of them as "setup" and "cleanup".
- componentWillMount (setup) is called only once in the component lifecycle, immediately before the component is rendered.
- componentWillUnmount (clean up) is the last function to be called immediately before the component is removed from the DOM. It is generally used to perform clean-up for any DOM-elements or timers created in componentWillMount.


## effects hook

#### example:
```
 // Similar to componentDidMount and componentDidUpdate:
  useEffect(() => {
    // Update the document title using the browser API
    document.title = `You clicked ${count} times`;
  });

```

### What does useEffect do?
 By using this Hook, you tell React that your component needs to do something after render. React will remember the function you passed (we’ll refer to it as our “effect”), and call it later after performing the DOM updates. In this effect, we set the document title, but we could also perform data fetching or call some other imperative API.


### We Placing useEffect inside the component to be able to access the  state variables (or any props) right from the effect


### useEffect run after every render