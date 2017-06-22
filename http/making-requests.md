# Making HTTP Requests
Your browser is set up to make GET requests whenever you type a URL into the address bar and hit enter.
The server that receives requests processes that specific request and renders specific information.

A common pattern in web development is using HTTP requests to communicate with servers and manipulate data.
There are several [HTTP request methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods) that can communicate with servers.
Let's examine GET requests.

Go to [https://jsonplaceholder.typicode.com/posts](https://jsonplaceholder.typicode.com/posts).
What do you see?.  Wouldn't it be great to use this already existing information to create a webpage?

## [Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)
The fetch API is built into most modern browsers.  It provides an easy way for developers to write requests to websites.
Please keep in mind that the fetch API is [asynchronous](https://stackoverflow.com/questions/748175/asynchronous-vs-synchronous-execution-what-does-it-really-mean).

```javascript
fetch('https://jsonplaceholder.typicode.com/posts/')
.then(res => res.json())
.then(posts => {
  // do things with your posts array here
  // perhaps we can display some of that information on your webpage
});
```

Remember [DOM manipulation](../dom/dom-manipulation.html)?  Great! Let's combine that with a fetch request to display information about the posts.

# Class Exercise
1. Create a new file in your text editor.
2. Use the fetch template above to fetch post information.
3. Display relevant post information to the webpage.  A simple unordered list is fine.

# Homework
1. Take a look around [JSONPlaceHolder](https://jsonplaceholder.typicode.com/) and use their API to create a sample website.

# Resources
1. [Fetch API](https://www.youtube.com/watch?v=g6-ZwZmRncs)
2. [Public APIs](https://github.com/toddmotto/public-apis) - a collective list of free JSON APIs for use in web development.
