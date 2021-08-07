## Review, Research, and Discussion

### Name 5 Javascript UI Frameworks (other than React)
1- Angular.
2- Vue.js
3- Ember.js
4- Meteor
5- Mithril

### What’s the difference between a framework and a library?
[ref](https://sofienebk.medium.com/what-is-the-difference-between-a-framework-and-library-2b712a1a1c41)
When you use a library, you are in charge of the application flow. You choose when and where to call the library. When you use a framework, the framework is in charge of the flow. It provides you with a few places to plug in your code, but it calls the code you plugged in as needed.

## Term

### Rendering
[wikipedia](https://en.wikipedia.org/wiki/Software_rendering)
- Software rendering is the process of generating an image from a model by means of computer software.
- In the context of computer graphics rendering, software rendering refers to a rendering process that is not dependent upon graphics hardware ASICs, such as a graphics card.


### Templates
[ref](https://www.computerhope.com/jargon/t/template.htm)
is a file that is created with an overall layout to be used with one or more documents.

### State
[ref](https://www.geeksforgeeks.org/reactjs-state-react/)
The state is an instance of React Component Class can be defined as an object of a set of observable properties that control the behavior of the component. In other words, the State of a component is an object that holds some information that may change over the lifetime of the component.




## react hello world
[ref](https://reactjs.org/docs/introducing-jsx.html)

### react : is a JavaScript library
#### the smallest examplein react is:
```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```


### Introducing JSX:

```
const element = <h1>Hello, world!</h1>;
```
this syntax is called JSX, and it is a syntax extension to JavaScript

#### Why JSX?
Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both

### Embedding Expressions in JSX:

```
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;

ReactDOM.render(
  element,
  document.getElementById('root')
);
```
as you can see, we use the variable **name** inside curly braces{}, You can put any valid JavaScript expression inside the curly braces in JSX.


#### Specifying Attributes with JSX:
- **quotes " "** for string values
```
const element = <div tabIndex="0"></div>;
```

- **curly braces {}** for expressions
```
const element = <img src={user.avatarUrl}></img>;
```

#### JSX Represents Objects

```
// Note: this structure is simplified
const element = {
  type: 'h1',
  props: {
    className: 'greeting',
    children: 'Hello, world!'
  }
};
```
These objects are called “React elements”. You can think of them as descriptions of what you want to see on the screen. React reads these objects and uses them to construct the DOM and keep it up to date.


### Rendering Elements 

#### React elements are the smallest building blocks of React apps. they are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.
```
const element = <h1>Hello, world</h1>;
```

### Rendering an Element into the DOM

```
<div id="root"></div>
```
We call this a “root” DOM node because everything inside it will be managed by React DOM. reacts apps are usually have single “root” DOM node and to To render a React element into a root DOM node, pass both to ReactDOM.render():

```
function tick() {
  const element = (
    <div>
      <h1>Hello, world!</h1>
      <h2>It is {new Date().toLocaleTimeString()}.</h2>
    </div>
  );
  ReactDOM.render(element, document.getElementById('root'));
}

setInterval(tick, 1000);
```



