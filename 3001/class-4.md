# Forms
[reactjs.org](https://reactjs.org/docs/forms.html)

## What is a ‘Controlled Component’?

In React, mutable state is typically kept in the state property of components, and only updated with setState().
We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. **An input form element whose value is controlled by React in this way is called a “controlled component”**.

### Example: form log the name when it is submitted using controlled component:

``` html
class NameForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: ''};

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }

  handleChange(event) {
    this.setState({value: event.target.value});
  }

  handleSubmit(event) {
    alert('A name was submitted: ' + this.state.value);
    event.preventDefault();
  }

  render() {
    return (
      <form onSubmit={this.handleSubmit}>
        <label>
          Name:
          <input type="text" value={this.state.value} onChange={this.handleChange} />
        </label>
        <input type="submit" value="Submit" />
      </form>
    );
  }
}
```

## The textarea Tag
In React, a &lt;textarea&gt; uses a value attribute

```html
class EssayForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      value: 'Please write an essay about your favorite DOM element.'
    };
```

## The select Tag
for example to make a drop-down list in html, you will use the **selected attribute** to make asny option you want is initially selected.In React, we don't use **selected attribute**, instead it uses a **value attribute** on the root select tag. This is more convenient in a controlled component because you only need to update it in one place. 

### Example: creat make a drop-down list with initially value of "Coconut":
- HTML

```html
<select>
  <option value="lime">Lime</option>
  <option selected value="coconut">Coconut</option>
</select>
```

- React

```html
class FlavorForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: 'coconut'};

    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }
```

## The file input Tag
file tag is **uncontrolled** component in React because it only reading file.


## Handling Multiple Inputs
to handle multiple controlled input elements, add a **name attribute** to each element and let the handler function choose based on the value of **event.target.name**.

## How do we target what the user is entering if we have an event handler on an input field?
- In React, mutable state is kept in the state property of components, and only updated with **setState()**
- handler runs on every keystroke to update the React state, the displayed value will update as the user types.

# The Conditional (Ternary) Operator Explained

## Why would we use a ternary operator?
Shorten your if statements into one line of code with the conditional operator


## Rewrite the following statement using a ternary statement:

```html
  if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }
```
#### solution:
 x===y ? console.log(true) : console.log(false)
