# REACT

With React, you can create components, or chunks of HTML code that can render differently based on javascript, or JSX.

+ Render method returns a description of what you see on screen, and react displays this to you.

+ You can compose and render custom DOM components that you create (bundle up HTML elements into one DOM element)

## JSX

React uses JSX langguage, which is markup and Javascript in one.

You can call any valid javascript expression inside curly brackets and insert them into HTML elements

JSX can be used inside loops, if statements, functions, etc - it becomes part of javascript.

JSX elements can contain HTML parent/child relationships.

<div>
    <h2>Hello!</h2>
    <h2>Nice to see you</h2>
<div>

(source: https://reactjs.org/docs/introducing-jsx.html)

React DOM escapes values embedded in JSX, which means that content is not open to attacks.

Use React.createElement() to create an object.

## Rendering Elements

A "root" DOM node in React is called a "root" because everything inside of it will be managed by React DOM.

To render a React element to a root DOM node, pass both to React.DOM.render():

const element = <h2>Hello, world</h2>
ReactDOM.render(element, document.getElementById('root'));

(source: https://reactjs.org/docs/rendering-elements.html)

## Components

Components let you split a UI into discrete pieces and utilize them in isolation.

+ Needs to accept single proprty (props), and returns a React element.

+ You can use user-defined components (ie using a word like "welcome" instead of HTML stuff like h1 or div).

+ You can split React Components into smaller components.

+ Props of React components must be pure (must not attempt to change their inputs).
