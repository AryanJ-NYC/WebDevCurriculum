# Common JavaScript syntax

## Variable declarations
```javascript
var PI = 3.14159;
var willChange = 2;
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
for (var i = 0; i < someArray.length; i++) {
    doSomething(i);
}
```

## Functions
```javascript
function myFunction (a, b) {
    return a * b;
}
```
OR

```javascript
var myFunction = function (a, b) {
    return a * b;
}
```

Please keep in mind that we can pass functions as arguments. This is a common source of confusion.
See question 2 below for practice with this.

```javascript
function doer (functionArg, elementArg1, elementArg2) {
  return functionArg(elementArg1, elementArg2);
}

function sum (a, b) {
  return a + b;
}

function difference (a, b) {
  return a - b;
}

var a = 7,
    b = 5;

doer(sum, a, b); // returns 12
doer(difference, a, b); // returns 2
```

## Objects
```javascript
var objName = {
    key1: 1,
    schoolName: 'Queens College',
    sum: function (a, b) {
        return a + b;
    }
}

var one = objName[key1]; // note one way to access object key's
var two = 2;
var sum = objName.sum(one, two); // note the other way of accessing keys

console.log('I love ' + objName.schoolName);
// OR
console.log('I dislike ' + objName[schoolName]);
```
