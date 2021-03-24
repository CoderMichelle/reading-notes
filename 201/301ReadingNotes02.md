 State and Life Cycle

To update the UI in a singlefunction, use classes:

class Clock extends React.Component {
  render() {
    return (
      <div>
        <h1>Hello, world!</h1>
        <h2>It is {this.props.date.toLocaleTimeString()}.</h2>
      </div>
    );
  }
}

(source: https://reactjs.org/docs/state-and-lifecycle.html)
Lifecycle Methods

Lifecycle methods in React are code that runs when a timer sets when class component renders the DOM, and when it clears after running.

Component renders the DOM: mounting Component clears the DOM: unmounting

Using State:

    Do not modify directly (use setState())

    State Updates may be asynchronous
        Can batch multiple setState() calls into a single mounting update by giving setState() a function rather than an object

    State updates are merged

Handling Events

In React, you don't need to call addEventListener to add listeners to a DOm element after it is created, just provide a listener when element is initially rendered.

With ES6 classes, it is common for an event handler to be a method on the class.
Conditional Rendering

You can render different components based on the state of your application using if or the conditional operator

One of these will be called:

function UserGreeting(props) {
  return <h1>Welcome back!</h1>;
}

function GuestGreeting(props) {
  return <h1>Please sign up.</h1>;
}

based on this:

function Greeting(props) {
  const isLoggedIn = props.isLoggedIn;
  if (isLoggedIn) {
    return <UserGreeting />;
  }
  return <GuestGreeting />;
}

(source: https://reactjs.org/docs/conditional-rendering.html)

Inline If-Else

condition ? true : false

like this:

render() {
  const isLoggedIn = this.state.isLoggedIn;
  return (
    <div>
      The user is <b>{isLoggedIn ? 'currently' : 'not'}</b> logged in.
    </div>
  );
}

render() {
  const isLoggedIn = this.state.isLoggedIn;
  return (
    <div>
      {isLoggedIn
        ? <LogoutButton onClick={this.handleLogoutClick} />
        : <LoginButton onClick={this.handleLoginClick} />
      }
    </div>
  );
}
