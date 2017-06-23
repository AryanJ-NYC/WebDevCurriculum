# [Lifecycle](https://facebook.github.io/react/docs/react-component.html#the-component-lifecycle)
All components have a lifecycle that reflects their existence in the DOM.  React
provides "lifecycle methods" which allow developers to run code at specific times in the process.

Please visit the React documentation and review the [component lifecycle documentation](https://facebook.github.io/react/docs/react-component.html#the-component-lifecycle).

## Fetch in React
The `fetch()` method is normally run in the [`componentDidMount()`](https://facebook.github.io/react/docs/react-component.html#componentdidmount) method 
(which is called after the component mounted the DOM).  For example:

### src/Posts.js
```jsx
import React, { Component } from 'react';

class Posts extends Component {
  constructor() {
    super();
    this.state = { posts: [] };
  }

  componentDidMount() {
    const url = 'https://www.reddit.com/r/aww.json';

    fetch(url)
    .then(res => res.json())
    .then(json => json.data.children)
    .then(posts => {
      this.setState({ posts: posts });
    });
  }
  
  render() {
    const postElements = this.state.posts.map(post => {
      const postData = post.data;

      return (
        // should be extracted into a separate component
        <a href={`https://www.reddit.com${postData.permalink}`} key={postData.id}>
          <div>
            <img src={postData.thumbnail} alt={postData.title} />
            <span>{postData.title}</span>
          </div>
        </a>
      );
    });

    return <div>{postElements}</div>;
  }
}

export default Posts;
```
