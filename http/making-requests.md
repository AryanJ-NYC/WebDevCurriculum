# Making HTTP Requests
Your browser is set up to make GET requests whenever you type a URL into the address bar and hit enter.
The server that receives requests processes that specific request and renders specific information.

A common pattern in web development is using HTTP requests to communicate with servers and manipulate data.
There are several [HTTP request methods](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods) that can communicate with servers.
Let's examine GET requests.

Go to [http://pokeapi.co/api/v2/pokemon-species/pikachu](http://pokeapi.co/api/v2/pokemon-species/pikachu/).
What do you see?.  Wouldn't it be great to use this already existing information to create a webpage?

## [Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)
The fetch API is built into most modern browsers.  It provides an easy way for developers to write requests to websites.
Please keep in mind that the fetch API is [asynchronous](https://stackoverflow.com/questions/748175/asynchronous-vs-synchronous-execution-what-does-it-really-mean).

```javascript
fetch('https://pokeapi.co/api/v2/pokemon-species/pikachu/')
.then(res => res.json())
.then(pokemon => {
  // do things with your pokemon object here
  // perhaps we can display some of that information on your webpage
});
```

Remember [DOM manipulation](../dom/dom-manipulation.html)?  Great! Let's combine that with a fetch request to display information about our Pokemon.

# Class Exercise
The following exercise must be done using 100% DOM manipulation. Do **not** modify *index.html*.
1. Open a new Thimble project or use your text editor (it is preferred you use a text editor as it's better practice)
2. Use the fetch template above to fetch information about your favorite Pokemon.
3. Display relevant Pokemon information to the webpage.  A simple unordered list is fine.
