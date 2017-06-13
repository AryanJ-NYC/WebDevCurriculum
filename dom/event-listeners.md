# Event Listeners
Users must be able to interact with a webpage for any type of meaningful experience.
These interactions come in the form of clicks, key presses, mouse movements, etc.
We can think of these interactions as *events* (though events are not always triggered by the user).
We can *add event listeners* to our HTML elements to respond to an event.

Study the [`addEventListener()` documentation](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener).
The `addEventListener()` method takes two parameters: an [event type](https://developer.mozilla.org/en-US/docs/Web/Events) (entered as a string) to listen for and a listener (normally a function that responds to the event).

# Example
Type the following into your console:
```javascript
document.getElementById('event-listeners').addEventListener('click', function (event) {
  const elem = event.target;
  if (confirm('Do you want it to happen?')) {
    elem.style.color = 'red';
    elem.innerText = 'IT\'S HAPPENING!';
    const img = document.createElement('img');
    img.setAttribute('src', 'https://media.giphy.com/media/rl0FOxdz7CcxO/giphy.gif');
    elem.appendChild(img);
  }
  console.log(event);
});
```
## What Just Happened?
It happened.

## No, Seriously
As described in the [previous lesson](./dom-manipulation.html), we access the element with the `id` *event-listeners*.
Then, we add an *event listener* for the click event to the element that was accessed.
The listener is a function that runs when the event is triggered.

# Class Exercise
The following exercise must be done using 100% DOM manipulation. Do **not** modify *index.html*.
1. Load your code from the [previous lesson](./dom-manipulation.html)'s exercise.
2. Delete the second button and move the first button to the bottom of the page.
3. Create an [`input`](https://www.w3schools.com/tags/tag_input.asp) element.
4. Set the [`input` type](https://www.w3schools.com/html/html_form_input_types.asp) of the [`input` element](https://www.w3schools.com/tags/tag_input.asp).to *text*.
5. Append the `input` element to the *main-div* **before** the button is appended.
6. Add a click event listener to the button that takes the `value` of the `input` tag and appends it to the unordered list.

For a better user experience, the `value` of the input tag should be cleared when button is clicked.

# Homework
1. Add an event listener so the user can hit enter on the keyboard to add to the list.

# Resources
* [addEventListener() - Beau teaches JavaScript](https://www.youtube.com/watch?v=F3odgpghXzY&list=PLWKjhJtqVAbllLK6r2dnGjUVWB_cFNcuO&index=4)
