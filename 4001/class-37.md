## Why choose Redux instead of the Context API for global state?
[ref](https://academind.com/tutorials/reactjs-redux-vs-context-api/)
he Context API (currently) is not built for high-frequency updates (quote of Sebastian Markbage, React Team), it’s not optimized for that. The react-redux people ran into this problem when they tried to switch to React Context internally in their package.


## What is the purpose of a reducer?
[ref](https://css-tricks.com/understanding-how-reducers-are-used-in-redux/#:~:text=A%20reducer%20is%20a%20function,receives%20to%20determine%20this%20change.&text=Redux%20relies%20heavily%20on%20reducer,to%20execute%20the%20next%20state.)
A reducer is a function that determines changes to an application’s state. It uses the action it receives to determine this change.


## What does an action contain?
Actions are the only source of information for the Store. Actions carry the information that sends data from the application to the Store.


## Why do we need to copy the state in a reducer?
The reducer needs to be a pure function without any side-effects. It should only take in an action and return the new state.


## Term


### immutable state
This allows the state to only change when absolutely necessary to make React apps perform as well as possible.

### time travel in redux
[ref](https://blog.scottlogic.com/2017/03/09/relogic-2.html#:~:text=Time%20travel%20is%20the%20ability,is%20always%20exactly%20the%20same.)
 the ability to move back and forth among the previous states of an application and view the results in real time. With Redux, given a specific state and a specific action, the next state of the application is always exactly the same

### action creator
[ref](https://css-tricks.com/understanding-how-reducers-are-used-in-redux/#:~:text=A%20reducer%20is%20a%20function,receives%20to%20determine%20this%20change.&text=Redux%20relies%20heavily%20on%20reducer,to%20execute%20the%20next%20state.)
An action is an object that contains two keys and their values. The state update that happens in the reducer is always dependent on the value of action.
### reducer
[ref](https://css-tricks.com/understanding-how-reducers-are-used-in-redux/#:~:text=A%20reducer%20is%20a%20function,receives%20to%20determine%20this%20change.&text=Redux%20relies%20heavily%20on%20reducer,to%20execute%20the%20next%20state.)
A reducer is a function that determines changes to an application’s state. It uses the action it receives to determine this change.
### dispatch
[ref](https://redux.js.org/api/store)
Dispatches an action. This is the only way to trigger a state change.
The store's reducing function will be called with the current getState() result and the given action synchronously. Its return value will be considered the next state. It will be returned from getState() from now on, and the change listeners will immediately be notified.


## CombineReducers
[Redux Docs: Using Combined Reducers](https://redux.js.org/usage/structuring-reducers/using-combinereducers/)
a utility function to simplify the most common use case when writing Redux reducers. You are not required to use it in your own application, and it does not handle every possible scenario. It is entirely possible to write reducer logic without using it, and it is quite common to need to write custom reducer logic for cases that combineReducer does not handle


### Defining State Shape

##### There are two ways to define the initial shape and contents of your store's state
- CreateStore function can take preloadedState as its second argument.
- The other way is for the root reducer to return the initial state value when the state argument is undefined

##### combineReducers takes an object full of slice reducer functions, and creates a function that outputs a corresponding state object with the same keys. This means that if no preloaded state is provided to createStore, the naming of the keys in the input slice reducer object will define the naming of the keys in the output state object.


## combineReducers(reducers)
he combineReducers helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.

The resulting reducer calls every child reducer, and gathers their results into a single state object. The state produced by combineReducers() namespaces the states of each reducer under their keys as passed to combineReducers()

#### Arguments
- reducers (Object): An object whose values correspond to different reducing functions that need to be combined into one.

- Returns#
(Function): A reducer that invokes every reducer inside the reducers object, and constructs a state object with the same shape.