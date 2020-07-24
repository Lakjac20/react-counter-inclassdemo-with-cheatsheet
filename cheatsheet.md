# Career Choice React Cheatsheet

+ If I want to render some JSX on the page:
    - I will call ReactDOM.render, and pass it the top-level element or component I want rendered, and the element (already on the page) to append this to.
    ```js
    ReactDOM.render(element, parentElement)
    ```

+ If I want multi-line JSX:
    - I will wrap the whole JSX expression in parentheses.

## Components

+ If I want just a simple component, perhaps taking some inputs, but only giving the output, and not requiring anything fancy:
    - I will write a functional component.
+ If I want a *smart* component, perhaps maintaining its own internal logic and data (state):
    - I will write a class component.

+ If I have some unique input which I want each instance of this component to have:
    - I will create a prop in the JSX (looks like HTML attribute), and in my component definition, I will accept those props as the `props` parameter (in a functional component) or `this.props` (in a class component). My "attribute name" from the JSX will be the property name in the `props`/`this.props` object.
+ If I need a prop to be a string, I will write it like this: `name="some string"`.
+ If I need a prop to be the value of a variable, I will write it like this: `name={variableName}`.
+ If I need a prop to be anything other than a string literal, I write it inside of curly braces (as above). 
    - For an array literal, I would do: `name={[1,2,3,4]}`.
    - For an object literal, I would do: `name={{ name="DMG", tea: "Ginseng & Ginger" }}`.
    - For a callback function, I would do: `name={nameOfCallbackFunction}` (note I am not *calling* the callback function here with parens).
+ If I want to inject any arbitrary JavaScript expression into the middle of JSX (anywhere), I will use the curlies, as well: `<div>{this.props.username}</div>` or `<div>{ Math.floor(Math.random() * 10) + 1 }</div>`.

