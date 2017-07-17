# SyncState
re-base's [`syncState()`](https://github.com/tylermcginnis/re-base#syncstateendpoint-options)
method makes it easy to bind Firebase and React.  That is,
when a change occurs to either the Firebase database or the React component,
the change is reflected on the other.

Using [`syncState()`](https://github.com/tylermcginnis/re-base#syncstateendpoint-options)
in a React component is easy. Let's use the [`List.js`](../react/state.html#srclistjs) from the React chapter as an example.

At the top of the file, import `base` from the [previous section](./intro.html#srcrebasejs):
```bash
import base from './rebase';
```

Then, in `List.js`'s [`componentDidMount()`](https://facebook.github.io/react/docs/react-component.html#componentdidmount)
method, do the following to sync the List component's state with Firebase:
```jsx
componentDidMount() {
  this.ref = base.syncState('list', {
    context: this,
    state: 'list',
    asArray: true
  });
}
```
That's it! Your list is now synced with Firebase.
