`console.log('Hello, World!')`

# Common JavaScript syntax

## Variable declarations
Use `const` for values that cannot change.  Use `let` otherwise.

Rule of thumb: Always use `const` unless absolutely necessary.

```javascript
const PI = 3.14159;
let willChange = 2;
```

Maybe you're wondering about value types.  Read [this](http://stackoverflow.com/questions/964910/is-javascript-an-untyped-language) for an explanation.

## If/else statement
```javascript
if (booleanExpression) {
    doSomething();
} else if (otherBooleanExpression) { 
    doSomethingElse();
} else {
    doThatLastThing();
}
```

## While loop
```javascript
while (booleanExpression) {
    doSomething();
}
```

## For loop
```javascript
for (let i = 0; i < someArray.length; i++) {
    doSomething(i);
}
```

## Functions
```javascript
function myFunction(a, b) {
    return a * b;
}
```
OR

```javascript
const myFunction = function (a, b) {
    return a * b;
}
```

## Objects
```javascript
let objName = {
    key1: 1,
    schoolName: 'Queens College',
    sum: function (a, b) {
        return a + b;
    }
}

const one = objName[key1]; // note one way to access object key's
const two = 2;
let sum = objName.sum(one, two); // note the other way of accessing keys

console.log('I love ' + objName.schoolName);
// OR
console.log('I dislike ' + objName[schoolName]);
```

# Enough Reading, Let's Code!
We will use [repl.it](https://repl.it/languages/javascript) to run the JavaScript code. It's suggested you save your examples to a `.js` file.

1. Write a function that logs the numbers from 1 to n. For multiples of three, log "Fizz" instead of that number.  For the multiples of five, log "Buzz" instead of that number. For multiples of both three and five, log "FizzBuzz" instead.
2. Write two functions, one named `celsiusToFahrenheit` and the other named `fahrenheitToCelsius.`  `celsiusToFahrenheit` should take in a celsius temperature as an argument and convert it to fahrenheit. Similarly, `fahrenheitToCelsius` should take in a fahrenheit temperature as an argument and convert it to celsius.

# Homework
1. Complete the JavaScript section of [Codecademy](https://www.codecademy.com/learn/javascript).
2. Get as far as possible in the JavaScript section of [Free Code Camp](http://www.freecodecamp.com).
