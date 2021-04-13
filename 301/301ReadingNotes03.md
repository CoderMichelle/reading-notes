LIFTING UP STATE

You can lift the state of multiple components up to a shared ancestor, so that they may allbe changed based on the same changing data.

    Easier to isolate and fix bugs

    If something can be derived from either props or state, it probably shouldn't be in the state

    For example, Instead of storing both Celsius and Fahrenheit values, you can store one temperature value and it's scale. And calculate value of each in conversion functions in render().

On Child Component:

    Instead of this.state.________, use this.props.________

    Instead of this.setState(), use this.props.on_______Change()

On Parent Component:

    React calls the function specified as onChange on the DOM .

LISTS and KEYS

You can build collections of elements and include them in JSX using curly braces.

map() syntax:

const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>
  <li>{number}</li>
);

ReactDOM.render(
  <ul>{listItems}</ul>,
  document.getElementById('root')
);

(source: https://reactjs.org/docs/lists-and-keys.html (Links to an external site.))

The code above is the same as this, which is in component format:

function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    <li>{number}</li>
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

Keys

Need to establish a key for list items:

const todoItems = todos.map((todo) =>
  <li key={todo.id}>
    {todo.text}
  </li>
);

    If you extract a list item component, you should keep the key on the <ListItem /> elements in the array rather than on the <li> element in the list item itself

    Keys must be unique to their siblings (other elements in list), but do not need to be globally unique

Map() Syntax, AGAIN:

function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    <ListItem key={number.toString()}
              value={number} />
  );
  return (
    <ul>
      {listItems}
    </ul>
  );
}

The Spread Operator

Quick syntax for adding items to arrays, combining arrays or objects, and spreading an array out into a function's argument.

When ...arr is used in a function call, it expands an iterable object arr into the list of arguments.

This doesn't work because the function is expecting multiple arguments:

Math.max([1,3,5]);

This does work because separate arguments:

Math.max(1,3,5);

This works, because spread operator:

Math.max(...[1,3,5]);

Also useful for:

    Copying an array
    Concatenating or combining arrays
    Using Math functions
    Using an array as arguments
    Adding an item to a list
    Adding to state in React
    Combining objects
    Converting NodeList to an array

Combining arrays:

const arrayOne = [1,2,3,4,5];
const arrayTwo = [6,7,8,9,10];
const arrayBoth = [...arrayOne,...arrayTwo];
console.log(...arrayBoth);

In math functions like Math.min() or Math.max(), which expect a list of arguments, not an array:

const numbers = [37, -17, 7, 0]
console.log(Math.min(numbers)) // NaN
console.log(Math.min(...numbers)) // -17
console.log(Math.max(...numbers)) // 37

(source: https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab (Links to an external site.))

Adding items to array:

const arrayOne = [3,4,5];
const arrayMore = [1,2,...arrayOne];
console.log(arrayMore);
