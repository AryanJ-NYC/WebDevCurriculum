# React Router
Components make React extremely powerful. React Router is a set of components that allows React components to be linked together.

## Installation
```bash
npm install react-router-dom 
```

## Basics
Use the [`Posts.js`](./lifecycle.html#srcpostsjs) example from the previous section.

Let's create a home page, an about page and a navbar (which contains links to the home and posts pages).

### src/Home.js
```jsx
import React, { Component } from 'react';

class Home extends Component {
  render() {
      return (
      <h2>Da Coolest Website Evar</h2>
    );
  }
}

export default Home;
```

### src/About.js
```jsx
import React, { Component } from 'react';

class About extends Component {
  render() {
    const name = this.props.match.params.name;
    return (
      <div>
        <h2>Welcome to <span className="text-capitalize">{name}'s</span> page!</h2>
        <p className="lead">This webpage is all about <span className="text-capitalize">{name}</span>.</p>
        <p>Want to learn more about <span className="text-capitalize">{name}</span>?</p>
        <p>Write a quick email to <a href={`mailto:${name}@${name}.com`}>{name}@{name}.com</a></p>
      </div>
    );
  }
}

export default About;
```

### src/Navbar.js
```jsx
import React, { Component } from 'react';
import { Link } from 'react-router-dom';

class Navbar extends Component {
  render() {
    return (
      <nav className="navbar navbar-default">
        <div className="container-fluid">
          <div className="navbar-header">
            <Link to="/" className="navbar-brand">My Page</Link>
          </div>
          <ul className="nav navbar-nav">
            <li>
              <Link to="/posts">Posts</Link>
            </li>
          </ul>
        </div>
      </nav>
    );
  }
}

export default Navbar;
```

## src/App.js
```jsx
import React, { Component } from 'react';
import { BrowserRouter as Router, Route } from 'react-router-dom'

import About from './About';
import Home from './Home';
import Navbar from './Navbar';
import Posts from './Posts';

class App extends Component {
  render() {
    return (
      <div>
        <Router>
          <div>
            <Navbar />
          
            <Route exact path="/" component={Home} />
            <Route path="/about/:name" component={About} />
            <Route path="/posts" component={Posts} />
          </div>
        </Router>
      </div>
    );
  }
}

export default App;
```

## Resources
* [React Router Documentation](https://reacttraining.com/)
