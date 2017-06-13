# DOM Manipulation
Let's try a quick example.  Type the following into your browser's console:
```javascript
document.getElementById('dom-manipulation').innerText = 'it\'s happening!';
```
Now refresh your page.

What happened here?  The [DOM document object](https://www.w3schools.com/js/js_htmldom_document.asp) represents our webpage.
If we want to access or modify anything on the webpage, we do so through the document object.

The [*getElementById()*](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById) method takes in a string as a parameter.  It searches for and returns the element whose id matches the string parameter.

The [*innerText*](https://developer.mozilla.org/en-US/docs/Web/API/Node/innerText) property is exactly that: the inner text of the HTML element.  It can be modified.

There are numerous ways to access and modify webpages.
Study and play with the properties and methods of the [document object](https://www.w3schools.com/js/js_htmldom_document.asp).

What other methods and properties can we use to manipulate the DOM?

# Classwork
1. Use the console, *document* and *getElementById()* to change the color of the element with the id *document-object-model* to any color besides black.
2. Use the console, *document* and *getElementById()* to change the background color of the element with the id *document-object-model* to any color besides black.
3. Change the font size of the elements with the class name *normal* to 16px.  This one's a bit tougher.  Make sure you understand the data structure your chosen method returns.

**Note:** These exercises require going into the DOM documentation as some necessary methods and properties were not described on this page.

# Class Exercise
## Setup

1. Create a new [Thimble](https://thimble.mozilla.org/en-US/) project or a new folder on your local machine (using your local machine is better practice for real-world projects).
2. Create an *index.html* file with the [standard HTML skeleton](http://webdev-gitbook-aryanj-nyc.c9users.io:8080/html/basics.html#standard-html-skeleton).
3. Create an *app.js* file in the same folder.
4. Add a [`script`](https://www.w3schools.com/tags/tag_script.asp) tag to the line before the closing `body` tag in *index.html* and link the *app.js* file using the `src` attribute
5. Open *index.html*.  Nothing should show.


## Exercise
The following exercise must be done using 100% DOM manipulation. Do **not** modify *index.html*.
1. Create a new `div` element (it may help to save the element to a variable).
2. Add a *main-div* `id` to your div element (you can use the [`setAttribute`](http://www.w3schools.com/jsref/met_element_setattribute.asp) method).
3. Append the new `div` element to the document.body.
4. Create a new `button` element.
5. Add some text to your button. The text can say whatever you want.
6. Append the button to *main-div*.
7. Create another `button` element.
8. Add some text to your new button. The text should be different than the first button.
9. Append the second button to the *main-div*. Reload `index.html` and you should see your two buttons.
10. Add the class *btn* to both of your buttons.
11. Create an `ul` (unordered list) element.
12. Append the `ul` element to the *main-div*.
13. Create three separate `li` (list) items.
14. Append the `li` items to the `ul`.
15. Add the class *list-item* to each of the `li` elements.
16. Add the `id` *main-list* to the `ul`.

Save this as you will continue to work on this in the [next lesson](./event-listeners.html).

# Resources
* [Selecting & Changing Website Elements (DOM manipulation) - Beau teaches JavaScript](https://www.youtube.com/watch?v=eaLKqoB9Fu0&list=PLWKjhJtqVAbllLK6r2dnGjUVWB_cFNcuO)
