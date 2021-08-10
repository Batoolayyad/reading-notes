## Review, Research, and Discussion


### How can we ensure that an effect hook runs only once?
[ref](https://css-tricks.com/run-useeffect-only-once/#:~:text=React%20has%20a%20built%2Din,componentDidMount%20%2C%20componentDidUpdate%20%2C%20and%20componentWillUnmount%20.)
use second param which is an array of variables that the component will check to make sure changed before re-rendering. You could put whatever bits of props and state you want in here to check against.

Or, put nothing:

```
useEffect(() => {
    // Run! Like go get some data from an API.
  }, []);
```
### Can useState() update more than one state variable at the same time?
[ref](https://reactjs.org/docs/hooks-state.html)

Declaring state variables as a pair of [something, setSomething] is also handy because it lets us give different names to different state variables if we want to use more than one.


You don’t have to use many state variables. State variables can hold objects and arrays just fine, so you can still group related data together. However, unlike this.setState in a class, updating a state variable always replaces it instead of merging it.

### Is useState() synchronous?
yes

## Term


### State Hook
[hooks-state](https://reactjs.org/docs/hooks-state.html) Links to an external site.) A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components. We’ll learn other Hooks later.


### Component Lifecycle
[the-lifecycle-of-a-react-component](https://medium.com/codex/the-lifecycle-of-a-react-component-8e01332a068d)
Each component goes through three phases: mounting, updating and unmounting. You can also think of it as our natural life cycle: we are born, we grow (adolescence and adulthood), and eventually, we die. React components are created by being mounted onto the DOM, they change or grow through updates, and finally, they can be removed or unmounted from the DOM. These three milestones are referred to as the React component lifecycle



## useReducer hook

[useReducer hook](https://reactjs.org/docs/hooks-reference.html#usereducer)

```
const [state, dispatch] = useReducer(reducer, initialArg, init);
```


an alternative to useState. Accepts a reducer of type (state, action) => newState, and returns the current state paired with a dispatch method

### How does useReducer work?
[guide-to-react-usereducer-hook](https://blog.logrocket.com/guide-to-react-usereducer-hook/)
useReducer is used to store and update states, just like the useState Hook. It accepts a reducer function as its first parameter and the initial state as the second.

useReducer returns an array that holds the current state value and a dispatch function, to which you can pass an action and later invoke. This is similar to the pattern Redux uses but with a few differences.

