# Common JavaScript syntax

## Variable declarations
Use `const` for values that cannot change.  Use `let` otherwise.

Rule of thumb: Always use `const` unless absolutely necessary.

```javascript
const PI = 3.14159;
let willChange = 2;
```

## [Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
```javascript
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }

  get area() {
    return this.calcArea();
  }

  calcArea() {
    return this.height * this.width;
  }
}

const square = new Rectangle(10, 10);
console.log(square.area); // 100
```

Similarly, in ECMAScript 5:
```javascript
function Rectangle (height, width) {
  this.height = height;
  this.width = width;
  this.area = height * width;
}

var square = new Rectangle(10, 10);
console.log(square.area); // 100
```

## [Arrow Functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)
These functions are commonly used in other functions.  For example:
```javascript
const arr = [1, 2, 3, 4, 5];
const squared = arr.map(elem => elem**2); // [2, 4, 9, 16, 25]
```
Please note:
1. If no brackets are used to surround the body, only one expression can be written and that expression will be returned.
2. A single parameter does not need to be wrapped in parentheses (though it can be).  Zero or multiple parameters must be wrapped in parentheses.

Similarly, in ECMAScript 5:
```javascript
var arr = [1, 2, 3, 4, 5];
var squared = arr.map(function (elem) {
   return elem ** 2; 
});
```

## [Template Literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)
This allows developers to finally use string interpolation.

```javascript
const pokemonName = 'bulbasaur',
      url = `https://pokeapi.co/api/v2/pokemon-species/${pokemonName}`; 
```

Similarly, in ECMAScript 5:
```javascript
var pokemonName = 'bulbasaur',
    url = 'https://pokeapi.co/api/v2/pokemon-species/' + pokemonName;
```

For more about the changes made from ES5 to ES6, visit [es6features](https://github.com/lukehoban/es6features).

# Classwork
1. Write a function that logs the numbers from 1 to n. For multiples of three, log "Fizz" instead of that number.  For the multiples of five, log "Buzz" instead of that number. For multiples of both three and five, log "FizzBuzz" instead.
2. [Action](https://github.com/AryanJ-NYC/web-curriculum/blob/master/lessons/javascript-fundamentals/functions-deep-dive/functions-exercises.md#q11-javascript-functions-7)
3. [Temperature Converter](https://github.com/AryanJ-NYC/web-curriculum/blob/master/lessons/javascript-fundamentals/functions-deep-dive/functions-exercises.md#q7-temperature-converter)
4. [Cat and Mouse](https://github.com/AryanJ-NYC/web-curriculum/blob/master/lessons/javascript-fundamentals/objects-and-arrays/objects-exercises.md#q6-javascript-simple-objects-3)

# Homework
1. Complete the JavaScript section of [Codecademy](https://www.codecademy.com/learn/learn-javascript).
2. Get as far as possible in the JavaScript section of [Free Code Camp](http://www.freecodecamp.com).

# Resources
* [Overview of ECMAScript 6 features](https://github.com/lukehoban/es6features)
* [ECMAScript 6 — New Features: Overview & Comparison](http://es6-features.org)
