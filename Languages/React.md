# Creating Elements

`const JSX = <h1>Hellow WOrld</h1>;`
assign the HTML to a JS property

```
const JSX = <div>
<ul><li></li></ul>
</div>;
```
You can also nest HTML elements; there has to be 1 root though

# Comments
Wrap around comment text with `{/* */}`

# Common Stuff
Feature|Syntax
--|--
Creating Elements|`const JSX = <h1><p>Hello WOrld</p></h1>;`
Comments|`{/* */}`
Rendering Components to DOM|`ReactDOM.render(<component>,<node>);`
Specify Node|`document.getElementById()` or any jQuery?
Rendering Classes to DOM|`ReactDOM.render(<class tag>,<node>);`

# Self Closing Tags
Every tag must be closed
Every tag may be self-closing `<br /`

# Components

## Stateless Functional Components
A component created by a JS Function that returns either JSX or Null
```
const MyComponent = function() {
  return (
    <div>E</div>
  )
}
```

One-lines: `const Camper = props => <p>{props.name}</p>`
## React Components with ES6
```
class Kitten extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <h1>Hi</h1>
    );
  }
}
```
Creates an ES6 Kitten class that extends the React.Component class
TO ensure proper initialization, call `super(props)` within the `constructor(props)` constructor

You put the JSX code you want to show up in the `render()` function

Type|Description
--|--
Stateless Function Component|function that accepts props and returns JSX
Stateless Component|Class that extends `React.Component` but does not change **state**
Stateful Component|Class that extends `React.Component` **and** changes state
## Composition
You can use the Class names similar to JSX tags; you can return `<Kitten />` and have the Kitten component be rendered from a different component

There is a Parent/Child relationship
Syntax of defining child components: `const TypesOfFruit = () => { }`

# Passing Properties

## Single Value
**Passing** a `user` property to `App`
```
<App>
  <Welcome user='Mark' />
</App>
```

For prop values to be **evaluated as JS** surrond in `{}`: `<currentDate date={Date()} />`

**Accessing** property: `const Welcome = (props) => <h1>Hello, {props.user}!</h1>`

Type|Syntax
--|-
Statless|`{props.user}`
ES6 Class|`{this.props.user}`

*May* have to wrap prop in `{}` especially if number when passing
## Array
Wrap in `{}` similar to JS elements
You can also `.join(", ")` to join all array elements
**Accessing** array : props.\<arr name>

## Default
```JSX
const MyComponent = (props) => {}
MyComponent.defaultProps = {location: "San Fran"};
```

Action|Syntax
--|--
Setting Default Props|`MyComponent.defaultProps = {<name>: <value>}`
Overriding|`<MyComponent name="Hello" />`
TypeChecking PropTYpes|`MyComponent.propTypes = {handleClick: PropTypes.func.isRequired}`

## TypeChecking
`MyComponent.propTypes = {handleClick: PropTypes.func.isRequired}`
1. Specifies handleClick is a function
2. Marks handleClick as required for the function

May need to import PropTypes via `import PropTypes from 'prop-types';`

# Statefulness

## Declaring
Declare within the constructor with `this.state = { }`

Action|Syntax
--|--
Declare in constructor|`this.state = {}`
Access in render()|`{this.state.<var>}`

## Rendering State
In render(): `{this.state.<var>}`
In render(), **before** return: you can put regular JS there
so you can do stuff like this 
```JSX
render() {
    const name = this.state.name
    return (
      <div>
			<h1>{name}</h1>
      </div>
    );
```

## Changing State
`this.setState({})` lets you modify state