# State
For components to be completely reusable and encapsulated, they must be able to initialize
and update their own private data or *state*.

Consider the class exercise from the [Event Listeners](../dom/event-listeners.html#class-exercise) section.
It was a list with an input field and a button that appended the value of the input field to the list.

Let's rewrite the list in React.

## src/List.js
```jsx
import React, { Component } from 'react';

class List extends Component {
  constructor() {
    super();
    this.state = { list: [] };
    this.addToList = this.addToList.bind(this);
  }

  addToList(event) {
    event.preventDefault();
    const itemToAdd = document.getElementById('item-to-add');
    if (itemToAdd.value) {
      const currentList = this.state.list.slice();
      currentList.push(itemToAdd.value);
      this.setState({ list: currentList });
      itemToAdd.value = '';
    }
  }

  render() {
    // this.state.list is an array of strings; need array of list items
    const listItems = this.state.list.map((item, index) => <li key={index}>{item}</li>);
    return (
      <div>
        <ul>
          {listItems}
        </ul>
        <form onSubmit={this.addToList}>
          <input type="text" id="item-to-add" />
          <button>Add to List</button>
        </form>
      </div>
    );
  }
}

export default List;
```

The `state` object is initialized in the constructor.  Note that `super()` must be the first line of the constructor.

The `setState` function [merges the provided object into the current state](https://facebook.github.io/react/docs/state-and-lifecycle.html#state-updates-are-merged).
This leaves other properties of the `state` object intact.  After merging the provided object into the current state,
it calls the `render()` function to learn what should be on the screen then manipulate the DOM accordingly.

Please note how the array of strings is made into an array of JSX list items in the `render()` function.

Note that we do not mutate `state` directly. As noted in the [React documentation],
we should *treat this.state as if it were immutable*.

# Classwork
1. Rename `List.js` to `TodoList.js`.
1. Remove the bullet points from the unordered list.
2. Create a new React component: `TodoItem.js`.
3. The `TodoItem` component should feature a checkbox that, when checked, toggles a boolean named `done`.
4. The boolean, when true, will cross out the text of the list.  If false, the strikethrough will not exist.
5. Instead of mapping the array items to `<li>` tags, map them to `<ListItem />` components passing in the appropriate `props`.
