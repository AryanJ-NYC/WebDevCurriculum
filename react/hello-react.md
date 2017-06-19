# Hello, React!
After setting up a new [Create React App](https://github.com/facebookincubator/create-react-app) application,
explore the folder structure and individual files.  We will start at `public/index.html`.

## `public/index.html`
`index.html` is a standard HTML skeleton with a container div that has an `id` of *root*.
The React application we build (which is comprised of several components that interact with each other) is "connected"
to the HTML page at the root div.  The connection is made in `src/index.js`.

## `src/index.js`
`src/index.js` has one responsibility: to render the React application to the HTML file.
The React application is imported from `src/App.js`.
Newer versions of `create-react-app` templates register a service worker that employs an offline-first caching strategy.
Visit the [React blog](https://facebook.github.io/react/blog/2017/05/18/whats-new-in-create-react-app.html#progressive-web-apps-by-default) for more information on the new service worker.

## `src/App.js`
The basic template for the React application goes here.

As you develop a React application, keep the [single responsibility principle](https://en.wikipedia.org/wiki/Single_responsibility_principle) in mind.
React applications conventionally use [presentational and container components](https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0).
