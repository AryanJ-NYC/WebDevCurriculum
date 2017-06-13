# Using CSS
```css
body {
  font-size: 12px;
  background-color: red;
}
```
OR

```html
<p style="font-size:12px;background-color:red">
  This is a paragraph with a red backgrund and 12px letters.
</p>
```

In the examples above, *body* and *p* are the **selectors**.
*font-size* and *background-color* are known as the **properties**.
*12px* and *red* are known as **values**.

What do selectors do? What about properties? What about values?

# Types of Selectors

## Elements
The **elements** selector styles ***ALL*** elements of a specific type.
Example:

```html
<p>I will be red.</p>
<p>Me too!</p>
```

```css
p {
  color: red;
}
```

## Classes
The **.class** selector styles all elements with the specified class.  As a convention, web developers use classes to select multiple HTML elements.  
Example:
```html
<p class="intro">This will have margins and a border!</p>
```

```css
.intro {
  margin-left: 10px;
  margin-right: 10px;
  border: 5px solid red;
}
```

## IDs
The **#id** selector styles the element with the specified id.  As a convention, web developers use IDs to *select* one specific element.  
Example:  
```html
<p id="myid">This will be cyan!</p>
```

```css
#myid {
  color: cyan;
}
```

# Properties and Values
Properties and value pairs define how an HTML element (whether selected by element, class or ID) should look.
Different properties expect different value types.  For example, [`background-color`](https://www.w3schools.com/cssref/pr_background-color.asp) expects an RGB value (though it can take other values)
while [`font-size`](https://www.w3schools.com/cssref/pr_font_font-size.asp) expects a numerical pixel value (though it can take others).
Visit the [W3 website](https://www.w3schools.com/cssref/default.asp) of the CSS property you're interested in to learn more about the large number of CSS properties.

# CSS Box Model
Please review the [CSS box model](https://www.w3schools.com/css/css_boxmodel.asp).

Learn more selectors [here](http://www.w3schools.com/cssref/css_selectors.asp).

# Classwork
1. Use [Thimble](https://thimble.mozilla.org/) to [create the Android logo](http://thecodeplayer.com/walkthrough/css3-android-logo) with only HTML and CSS.
2. Do the HTML & CSS track on [Codecademy](https://www.codecademy.com/)

# Homework
1. Complete the CSS section of [FreeCodeCamp](http://www.freecodecamp.com/).
2. Recreate the [Google homepage](https://www.google.com/).  Focus on the middle image and search bar; leave the header and footer for last.

# Resources
* [CSS Reference](http://www.w3schools.com/cssref/default.asp)