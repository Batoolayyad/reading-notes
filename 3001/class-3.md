# Lists and Keys
[reactjs.org]( https://reactjs.org/docs/lists-and-keys.html)


we use the map() function to take an array of numbers and double their values. We assign the new array returned by map() to the variable doubled and log it:



``` html

const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map((number) => number * 2);
console.log(doubled);
```


## Rendering Multiple Components

### what should I do If I want to loop through an array and display each value in JSX?
You can build collections of elements and include them in JSX using curly braces {}.

 We return a &lt;li&gt; element for each item and we assign the resulting array of elements to *listItems*, then include the listItems array inside a &lt;ul&gt; element, and render it to the DOM (*ReactDOM.render*):

 ``` html

 const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>
  <li>{number}</li>
);

ReactDOM.render(
  <ul>{listItems}</ul>,
  document.getElementById('root')
);

```

## Basic List Component

most of the time rundering a list going to be inside **Component**
### how to refactor the previous example into a component ?

Note:there will be a warning saying **a key should be provided for list items**, so we have to assign a key to the list items inside numbers.map().
#### “key”: is a special string attribute you need to include when creating lists of elements
``` html
function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    <li key={number.toString()}>
      {number}
    </li>
  );
  return (
    <ul>{listItems}</ul>
  );
}

const numbers = [1, 2, 3, 4, 5];
ReactDOM.render(
  <NumberList numbers={numbers} />,
  document.getElementById('root')
);

```



## Keys:
### what is key?
special string attribute you need to include when creating lists of elements.

### Keys Must Only Be Unique Among Siblings
but don’t need to be globally unique. We can use the same keys when we produce two different arrays.

### Keys don’t get passed to your components. 
If you need the same value in your component, pass it explicitly as a **prop** with a different name, in the below example Post component can read *props.id*, but *not props.key*.



```html 
const content = posts.map((post) =>
  <Post
    key={post.id}
    id={post.id}
    title={post.title} />
);
```


### What is the purpose of a key?
Keys help React identify which items have changed, are added, or are removed, so it give the element stable identity.
you can pick a key by using a string that uniquely identifies a list item among its siblings. usually we are using  *IDs from the data* as keys. But **only** if items have no stable IDs we use *item index* as a key.

- using IDs from the data:

```html
const todoItems = todos.map((todo) =>
  <li key={todo.id}>
    {todo.text}
  </li>
); 
```

- using item index:(**not recommend**)

```html
const todoItems = todos.map((todo, index) =>
  // Only do this if items have no stable IDs
  <li key={index}>
    {todo.text}
  </li>
);
```

## Extracting Components with Keys

 if you extract a ListItem component, you should keep the key on the &lt;ListItem&gt; elements in the array rather than on the &lt;li&gt; element in the ListItem itself:

 ```html
 function ListItem(props) {
  // Correct! There is no need to specify the key here:
  return <li>{props.value}</li>;
}

function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    // Correct! Key should be specified inside the array.
    <ListItem key={number.toString()} value={number} />
  );
  return (
    <ul>
      {listItems}
    </ul>
  );
}

const numbers = [1, 2, 3, 4, 5];
ReactDOM.render(
  <NumberList numbers={numbers} />,
  document.getElementById('root')
);
```

# Spread Operator
[coding at dawn](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

### what is the Spread Operator?
syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function’s arguments.

In JavaScript, spread syntax refers to the use of an ellipsis of three dots (…) to expand an iterable object into the list of arguments

### what Spread Operator can do?
- Copying an array
- Concatenating or combining arrays
- Using Math functions
- Using an array as arguments
- Adding an item to a list
- Adding to state in React
- Combining objects
- Converting NodeList to an array

## Examples:
### spread operator to combine two arrays:

```html
[...["😋😛😜🤪😝"]] // Array [ "😋😛😜🤪😝" ]
[..."🙂🙃😉😊😇🥰😍🤩!"] // Array(9) [ "🙂", "🙃", "😉", "😊", "😇", "🥰", "😍", "🤩", "!" ]

const hello = {hello: "😋😛😜🤪😝"}
const world = {world: "🙂🙃😉😊😇🥰😍🤩!"}

const helloWorld = {...hello,...world}
console.log(helloWorld) // Object { hello: "😋😛😜🤪😝", world: "🙂🙃😉😊😇🥰😍🤩!" }

```

### spread operator to add a new item to an array:

```html
const fewFruit = ['🍏','🍊','🍌']
const fewMoreFruit = ['🍉', '🍍', ...fewFruit]
console.log(fewMoreFruit) //  Array(5) [ "🍉", "🍍", "🍏", "🍊", "🍌" ]
```

### spread operator to combine two objects into one:

```html
const objectOne = {hello: "🤪"}
const objectTwo = {world: "🐻"}
const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}
console.log(objectThree) // Object { hello: "🤪", world: "🐻", laugh: "😂" }
const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}
objectFour.laugh() // 😂😂😂😂😂
```


# Pass Functions Between Components
[React - How to Pass Functions between Components](https://www.youtube.com/watch?v=c05OL7XbwXU)

### In the video, what is the first step that the developer does to pass functions between components?
creat the function wherever the state that we are going to change
### In your own words, what does the increment function do?
receiving the arrays item, loop through the array and find the matching one to update
### How can you pass a method from a parent component into a child component?
by passing it as passing it as a props
### How does the child component invoke a method that was passed to it from a parent component?
by using special attribute that attach to the component ( Refs. React)



