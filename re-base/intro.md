# re-base
React makes it easy for components to manage their own state.
Firebase makes it easy to set up a database quickly.
Since Firebase uses web sockets, it's easy to implement a database that two-way binds with React's state.
This means changes to the React component will sync with the Firebase database and
changes to the Firebase database will sync with the React component (without the need to refresh).

[re-base](https://github.com/tylermcginnis/re-base) is a library that makes syncing data
between React and Firebase easier.  There are many other React libraries that work with Firebase.
Feel free to explore others.

## Getting Started with Firebase and re-base in your React Application
To get started with re-base, carefully follow the instructions below:
1. Go to the [Firebase website](https://firebase.google.com/).
2. Click the *Get Started* button.
3. Click the *Add Project* button and submit the relevant information.
4. Click *Database* on the left sidebar
5. Click *Rules* on the top navbar.  Set both *read* and *write* properties to `true`.
6. Click the *Add Firebase to your web app* button and keep the modal open for reference for the eighth step.
7. Install `re-base` with:
```bash
npm install re-base --save
```
8. Create a new file in your React app's `src` folder named `rebase.js`.
Using the modal opened in step six, copy and paste the appropriate information:
## src/rebase.js

```js
import Rebase from 're-base';
import firebase from 'firebase/app';
import database from 'firebase/database';

// this variable's information should not be copy and pasted
// refer to your application's metadata
const app = firebase.initializeApp({
  apiKey: "AIzaSyinSeRtCraZYAPi-KeyHeREsahX7JU-zXc",
  authDomain: "this-is-my-project-id.firebaseapp.com",
  databaseURL: "https://this-is-my-project-id.firebaseio.com",
  projectId: "this-is-my-project-id"
});

const db = database(app);
const base = Rebase.createClass(db);

export default base;
```

You are ready to get started with Firebase in React!

## Resources
* [re-base API](https://github.com/tylermcginnis/re-base)
* [Examples using re-base](https://github.com/tylermcginnis/re-base/tree/master/examples)
