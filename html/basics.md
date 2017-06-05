[HTML Reference](http://www.w3schools.com/tags/default.asp)  
[Use Thimble to practice what you learn](https://thimble.mozilla.org/)  
[Use CodePen to practice what you learn](http://codepen.io)

# Standard HTML Skeleton
```html
<!DOCTYPE HTML>
<html>
  <head></head> <!-- meta information goes here -->
  <body></body> <!-- actual content goes here -->
</html>
```

# Tag Examples
```html
<p>This is a paragraph</p>
<h1>This is a heading</h1>
<a href="http://www.google.com">This is a link to Google.</a>
```

## [Links](https://www.w3schools.com/tags/tag_a.asp)
```html
<a href="http://www.google.com">This is a link to Google.</a>
```

## [Images](https://www.w3schools.com/tags/tag_img.asp)
```html
<img src="http://cdn2-www.dogtime.com/assets/uploads/gallery/30-impossibly-cute-puppies/impossibly-cute-puppy-8.jpg" alt="Cute dog" />
```

What is alt?

## [Input](https://www.w3schools.com/tags/tag_input.asp)
Input tags are those that accept user input.  There are many [types](https://www.w3schools.com/tags/att_input_type.asp) of possible user input.
Here are some common input types. Please review documentation to review other types.

### Text
```html
<label>First name: <input type="text" name="fname" /></label><br>
<label for="lname">Last name:</label> <input type="text" id="lname" name="last-name"><br>
```

Please note the two different ways to create a proper `label`.  What does `label` do?

### Password
```html
<label>Password: <input type="password" name="user-password" /></label>
```

### Checkbox
```html
<label><input type="checkbox" name="vehicle1" value="bike"> I have a bike</label><br>
<label><input type="checkbox" name="vehicle2" value="car"> I have a car</label><br>
<label><input type="checkbox" name="vehicle3" value="boat" checked> I have a boat</label><br>
```

### Radio Button
```html
<label><input type="radio" name="gender" value="male"> Male</label><br>
<label><input type="radio" name="gender" value="female"> Female</label><br>
<label><input type="radio" name="gender" value="other"> Other</label>
```

### File
```html
<label>Select a file: <input type="file" name="img"></label>
```

### Date
```html
<label>Birthday: <input type="date" name="bday"></label>
```

Try this tag in Google Chrome. Now Mozilla Firefox or Safari. What happens?

# Nested Tags  
```html
<div>
  <p>This is another paragraph</p>
</div>
```

# Lists

## Ordered List
```html
<ol>
  <li>Toast bread</li>
  <li>Put ham on bread</li>
  <li>Put cheese on bread</li>
  <li>Put both slices of bread together</li>
<ol>
```

## Unordered List
```html
<ul>
  <li>Bread</li>
  <li>Ham</li>
  <li>Cheese</li>
</ul>
```

# Classwork
1. Using [Thimble](https://thimble.mozilla.org/), write a shopping *list*.
2. Link elements of your shopping list to webpages. Challenge: how can we get the page to pop-up in a new tab?
3. Add a picture under each item of the list.
4. Add an input field to the bottom of the page.
5. Add a submit button (it won't work...yet) to the bottom of the page.
6. Make sure your code is well-organized (check that indendation!).
7. Copy and paste your HTML to a file named `index.html` on your local machine.
8. Open that file using your browser.

Create accounts at the following sites:

1. [FreeCodeCamp](http://www.freecodecamp.com/)
2. [Codecademy](https://www.codecademy.com/)

# Homework
1. Complete the HTML sections of [FreeCodeCamp](http://www.freecodecamp.com/) and [Codecademy](https://www.codecademy.com/learn/learn-html-css).
2. Experiment with HTML using [Thimble](https://thimble.mozilla.org/) or [CodePen](http://codepen.io).
