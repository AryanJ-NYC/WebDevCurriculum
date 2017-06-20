# Components
Components are reuasable and independent pieces of the user interface.  They accept
inputs known as `props` and return elements that describe what should be rendered on the screen.
Please note that the `props` object is **read-only**.

## Example
### src/Welcome.js
```javascript
import React, { Component } from 'react';

class Welcome extends Component {
  render () {
    return (
      <div>
        <p>Hello, {this.props.name}!</p>
      </div>
    );
  }
}

export default Welcome;
```
The `Welcome` component accepts a `props` argument called *name* and returns a React element
as shown above.

### src/App.js
```javascript
import React, { Component } from 'react';
import Welcome from './Welcome';

class App extends Component {
  render () {
    return (
      <div>
        <Welcome name="Mary" />
        <Welcome name="Bob" />
      </div>
    );
  }
}

export default App;
```

The `App` component renders a `div` component with two `Welcome` components as children.  
**Note:** A component must return a single root element.  In the example above, `<div>` is the root element.
