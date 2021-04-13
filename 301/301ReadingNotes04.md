## FORMS

In HTML, elements like <input>, <select>, etc maintain their own state and update it based on user input

In Reqact, mutable state is kept in the state property of components, and updated with setState()

To overcome this, make React state have priority "state of truth"

- A react component that renders a form also controls what hapens in that form on subsequent user input

Set value on an element to this.state.value:

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

(source: https://reactjs.org/docs/forms.html (Links to an external site.))

 

Multiple Inputs

    add a name attribute to each element and let the handler function choose what to do based on the value of event.target.name

class Reservation extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      isGoing: true,
      numberOfGuests: 2
    };

    this.handleInputChange = this.handleInputChange.bind(this);
  }

  handleInputChange(event) {
    const target = event.target;
    const value = target.type === 'checkbox' ? target.checked : target.value;
    const name = target.name;

    this.setState({
      [name]: value
    });
  }

 render() {
    return (
      <form>
        <label>
          Is going:
          <input
            name="isGoing"
            type="checkbox"
            checked={this.state.isGoing}
            onChange={this.handleInputChange} />
        </label>
        <br />
        <label>
          Number of guests:
          <input
            name="numberOfGuests"
            type="number"
            value={this.state.numberOfGuests}
            onChange={this.handleInputChange} />
        </label>
      </form>
    );
  }
}

Controlled Null Value

    A value prop set to null prevents the user from changing it

FORMS in BOOTSTRAP

The <FormControl> component renders a form control with Bootstrap styling. The <FormGroup> component wraps a form control with proper spacing, along with support for a label, help text, and validation state. To ensure accessibility, set controlId on <FormGroup>, and use <FormLabel> for the label.

<Form>
  <Form.Group controlId="formBasicEmail">
    <Form.Label>Email address</Form.Label>
    <Form.Control type="email" placeholder="Enter email" />
    <Form.Text className="text-muted">
      We'll never share your email with anyone else.
    </Form.Text>
  </Form.Group>

  <Form.Group controlId="formBasicPassword">
    <Form.Label>Password</Form.Label>
    <Form.Control type="password" placeholder="Password" />
  </Form.Group>
  <Form.Group controlId="formBasicCheckbox">
    <Form.Check type="checkbox" label="Check me out" />
  </Form.Group>
  <Button variant="primary" type="submit">
    Submit
  </Button>
</Form>

(source: https://react-bootstrap.github.io/components/forms/)
