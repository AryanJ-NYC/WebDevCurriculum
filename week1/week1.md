# HTML  
[HTML Reference](http://www.w3schools.com/tags/default.asp)  
[Practice what you learned](https://thimble.mozilla.org/)
## Tag Examples
`<p>This is a paragraph</p>`  
`<h1>This is a heading</h1>`  
`<a href="http://www.google.com">This is a link to Google.</a>`
## Nested Tags  
```html
<div>
  <p>This is another paragraph</p>
</div>
```
## Lists
### Ordered List
```html
<ol>
  <li>Toast bread</li>
  <li>Put ham on bread</li>
  <li>Put cheese on bread</li>
  <li>Put both slices of bread together</li>
<ol>
```
### Unordered List
```html
<ul>
  <li>Bread</li>
  <li>Ham</li>
  <li>Cheese</li>
</ul>
## Standard HTML Skeleton
```html
<! DOCTYPE HTML>
<html>
  <head></head> <!-- meta information goes here -->
  <body></body> <!-- actual content goes here -->
</html>
```
# CSS
[CSS Reference](http://www.w3schools.com/cssref/default.asp)
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
In the example above, *p* is the **selector**, *font-size* and *background-color* are known as the **properties** and *12px* and *red* are known as **values**.

## Classes
The .class selector styles all elements with the specified class.  As a convention, web developers use classes to *select* multiple HTML elements.  
Example:
`<p>This will have margins and a border!</p>`
```css
.intro {
  margin-left: 10px;
  margin-right: 10px;
  border: 5px solid red;
```
## IDs
The #id selector styles the element with the specified id.  AS a convention, web developers use IDs to *select* one specific element.  
Example:  
`<p id="myid">This will be cyan!</p>`
```css
  #myid {
    color: cyan;
  }
```


# Enough Reading, Let's Write!
Create accounts at the following sites:
1. [FreeCodeCamp](http://www.freecodecamp.com/)
2. [Codecademy](https://www.codecademy.com/)

# Homework
1. Complete the HTML & CSS sections of FreeCodeCamp and Codecademy.
2. Play with HTML & CSS using [Thimble](https://thimble.mozilla.org/).