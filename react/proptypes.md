# PropTypes
React has built-in typechecking on the props of components.  This typechecking helps developers catch bugs and broadcast to other developers exactly what data types components' props expect.

Consider the [`Welcome.js`](./components.html#srcwelcomejs) example from the components section with an added PropType:

```jsx
import React, { Component } from 'react';
import PropTypes from 'prop-types';

class Welcome extends Component {
  render () {
    return (
      <div>
        <p>Hello, {this.props.name}!</p>
      </div>
    );
  }
}

Welcome.propTypes = {
  name: PropTypes.string.isRequired
}

export default Welcome;
```

Try passing a non-string to the name prop or not passing the name prop at all.  Now check the console. Hooray for errors!

There are many PropTypes to consider. Refer to the [React documentation](https://facebook.github.io/react/docs/typechecking-with-proptypes.html) when using PropTypes.
