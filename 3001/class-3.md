# Lists and Keys

we use the map() function to take an array of numbers and double their values. We assign the new array returned by map() to the variable doubled and log it:



``` html

const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map((number) => number * 2);
console.log(doubled);
```


## Rendering Multiple Components

#### If I want to loop through an array and display each value in JSX, how do I do that in React?
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
**who to refactor the previous example into a component ?**

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
#### what is key?
special string attribute you need to include when creating lists of elements.

#### Keys Must Only Be Unique Among Siblings
but don’t need to be globally unique. We can use the same keys when we produce two different arrays.

#### Keys don’t get passed to your components. 
If you need the same value in your component, pass it explicitly as a **prop** with a different name, in the below example Post component can read *props.id*, but *not props.key*.



```html 
const content = posts.map((post) =>
  <Post
    key={post.id}
    id={post.id}
    title={post.title} />
);
```


#### What is the purpose of a key?
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




