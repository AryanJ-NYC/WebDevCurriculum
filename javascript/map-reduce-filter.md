Web development, including development with React, relies on fetching arrays of [JSON](https://www.w3schools.com/js/js_json_intro.asp) objects from web APIs.
Developers are expected to be able to sort, map, filter, reduce, etc. this data.

# [Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
The map() method takes in a function, *f*, as a parameter.
It returns a new array with the elements returned by the function *f*.

## Map Example 1
```javascript
var double = function (currentValue) {
  return currentValue * 2;
}

var someArray = [1, 2, 3, 4, 5];
var doubledArray = someArray.map(double); // [2, 4, 6, 8, 10]
```

Please note, the above can be also written as:
```javascript
var someArray = [1, 2, 3, 4, 5];
var doubledArray = someArray.map(function (currentValue) {
  return currentValue * 2;
});
```

## Map Example 2
```javascript
var famousSingers = [
  { firstName: 'Michael', lastName: 'Jackson' },
  { firstName: 'Elvis', lastName: 'Presley' },
  { firstName: 'David', lastName: 'Bowie' },
  { firstName: 'Bob', lastName: 'Dylan' },
  { firstName: 'Beyoncé', lastName: 'Knowles' },
];

// returns ["Michael Jackson", "Elvis Presley", "David Bowie", "Bob Dylan", "Beyoncé Knowles"]
var justNames = famousSingers.map(function (currSinger) {
  return currSinger.firstName + ' ' + currSinger.lastName;
});
```

# [Filter](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
The filter() method takes in a [predicate](https://en.wikipedia.org/wiki/Predicate_(mathematical_logic) as a parameter.
It returns a new array with elements that pass the predicate's test.

## Filter Example 1
```javascript
var someArray = [1, 2, 3, 4, 5];

// returns [2, 4]
var evenValues = someArray.filter(function (currValue) {
  return currValue % 2 === 0;
});
```

## Filter Example 2
```javascript
var topHomeRunHitters = var topHomeRunHitters = [
  { firstName: 'Barry', lastName: 'Bonds', numHomeRuns: 762 },
  { firstName: 'Hank', lastName: 'Aaron', numHomeRuns: 755 },
  { firstName: 'Babe', lastName: 'Ruth', numHomeRuns: 714 },
  { firstName: 'Alex', lastName: 'Rodriguez', numHomeRuns: 696 },
  { firstName: 'Willie', lastName: 'Mays', numHomeRuns: 660 },
];

/**
[
  { firstName: 'Barry', lastName: 'Bonds', numHomeRuns: 762 },
  { firstName: 'Hank', lastName: 'Aaron', numHomeRuns: 755 },
  { firstName: 'Babe', lastName: 'Ruth', numHomeRuns: 714 }
]
**/
var over700Club = topHomeRunHitters.filter(function (currPlayer) {
  return currPlayer.numHomeRuns > 700;
});
```

Given the *topHomeRunHitters* variable and the map() and filter() functions,
how would you create an array of strings comprised of the names (first and last) of baseball players with more than 700 home runs?

# [Reduce](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce?v=example)
The reduce() method takes in a function and runs it against an accumulator and each element of the array (in order).
It returns a new array with a single, reduced value (the final accumulator) after all elements have been run through the function.

## Reduce Example 1
```javascript
var someArray = [1, 2, 3, 4, 5];

// returns 15
var sum = someArray.reduce(function (accumulator, currValue) {
  return accumulator + currValue;
}, 0)
```

## Reduce Example 2
```javascript
var topHomeRunHitters = [
  { firstName: 'Barry', lastName: 'Bonds', numHomeRuns: 762 },
  { firstName: 'Hank', lastName: 'Aaron', numHomeRuns: 755 },
  { firstName: 'Babe', lastName: 'Ruth', numHomeRuns: 714 },
  { firstName: 'Alex', lastName: 'Rodriguez', numHomeRuns: 696 },
  { firstName: 'Willie', lastName: 'Mays', numHomeRuns: 660 },
];

// returns 3587
var totalHomeRuns = topHomeRunHitters.reduce(function (acc, currPlayer) {
  return acc + currPlayer.numHomeRuns;
}, 0);
```

Given the *topHomeRunHitters* variable and the filter() and reduce() functions,
how would you calculate the sum of the number of home runs hit by players with more than 700 home runs?

# Classwork
1. Implement [StringToNums](https://github.com/C4Q/web-curriculum/blob/master/lessons/javascript-fundamentals/advanced-array-methods/advanced-array-methods-exercises-2.md#q7-map-strings-to-nums)
2. Implement [Count Odds and Evens](https://github.com/C4Q/web-curriculum/blob/master/lessons/javascript-fundamentals/advanced-array-methods/advanced-array-methods-exercises-2.md#q12-count-odds-and-evens)
3. Get started with [Functional Programming with JavaScript](http://reactivex.io/learnrx/)
