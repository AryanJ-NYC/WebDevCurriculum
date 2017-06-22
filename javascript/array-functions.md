All section headers are linked to the appropriate documentation.  Use the links for more information.
# [Slice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)
## Syntax
```javascript
arrName.slice();
arrName.slice(start);
arrName.slice(start, end);
```
## Description
The `slice()` method returns a copy of the array.  It takes two *optional* parameters, the start of the slice and the end of the slice.  
If no parameters are passed to slice(), a copy of the array is returned.  
If one parameter, *start*, is passed to slice(), a copy of the string from *start* (inclusive) to the end of the string is returned.  
If two parameters are passed to slice(), *start* and *end*, a copy of the string from *start* (inclusive) to *end* (exclusive) is returned.

## Examples
```javascript
var arr = ['a', 'b', 'c', 'd'];
var copy = arr.slice(); // ['a', 'b', 'c', 'd']
var sliced = arr.slice(0, 2); // [a, b]
```

# [Splice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)
## Syntax
```javascript
arrName.splice(start);
arrName.splice(start, deleteCount);
arrName.splice(start, deleteCount, elementToAdd1, elementToAdd2, ...elementToAddN);
```

## Description
The `splice()` method adds or removes elements from an array and returns an array containing the deleted elements.  
It takes an infinite number of parameters.  
The first parameter, *start*, is the index where the splice begins.  
The second parameter, *deleteCount*, refers to the number of elements to delete.  
The next parameters, *elementToAdd1* through *elementToAddN*, adds those elements at index *start*.

## Examples
```javascript
var myFish = ['angel', 'clown', 'mandarin', 'sturgeon'];

myFish.splice(2, 0, 'drum', 'tuba'); // insert 'drum' at 2-index position
// myFish is ["angel", "clown", "drum", "tuba", "mandarin", "sturgeon"]

myFish.splice(2, 1); // remove 1 item at 2-index position (that is, "drum")
// myFish is ["angel", "clown", "mandarin", "sturgeon"]
```

# [Push](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push?v=example)
## Syntax
```javascript
 // all return length of arrName
arrName.push();
arrName.push(elementToAdd1, ..., elementToAddN);
```

## Description
The `push()` method adds one or more elements to the end of an array and returns the new length of the array.
It takes an infinite number of *optional* parameters, the elements to add.

## Examples
```javascript
var numbers = [1, 2, 3];
numbers.push(4);

console.log(numbers); // [1, 2, 3, 4]

numbers.push(5, 6, 7);

console.log(numbers); // [1, 2, 3, 4, 5, 6, 7]
```

# [Unshift](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift)
## Syntax
```javascript
 // all return length of arrName
arrName.unshift();
arrName.unshift(elementToAdd1, ..., elementToAddX);
```

## Description
The `unshift()` method adds one or more elements to the beginning of an array and returns the new length of the array.

## Examples
```javascript
var a = [1, 2, 3];
a.unshift(4, 5);

console.log(a); // [4, 5, 1, 2, 3]
```

# [Pop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop)
## Syntax
```javascript
arrName.pop();
```

## Description
The `pop()` method removes the last element from an array and returns that element.  This method changes the length of the array.

## Examples
```javascript
var a = [1, 2, 3];
a.pop(); // 3

console.log(a); // [1, 2]
```

# [Shift](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift)
## Syntax
```javascript
arrName.shift();
```

## Description
The `shift()` method removes the first element from an array and returns that element. This method changes the length of the array.

## Examples
```javascript
var a = [1, 2, 3];
var b = a.shift();

console.log(a); // [2, 3]
console.log(b); // 1
```

# [Concat](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat)
## Syntax
```javascript
arrToAddTo1.concat(arrToAdd1, arrToAdd2, ..., arrToAddN);
```

## Description
The concat() method is used to merge two or more arrays. This method does not change the existing arrays but instead returns a new array.

## Examples
```javascript
var arr1 = ['a', 'b', 'c'];
var arr2 = ['d', 'e', 'f'];

var arr3 = arr1.concat(arr2); // [ "a", "b", "c", "d", "e", "f" ]
```

# [Join](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join)
## Syntax
```javascript
arrName.join(); // if no parameter used, a comma (,) is used as glue
arrName.join(glue);
```

## Description
The `join()` method takes in one *optional* string parameter, *glue*, which is used to join all elements of an array into a string.

## Examples
```javascript
var a = ['Wind', 'Rain', 'Fire'];
a.join();    // 'Wind,Rain,Fire'
a.join('-'); // 'Wind-Rain-Fire'
```

# [IndexOf](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf)
## Syntax
```javascript
arrName.indexOf(needle);
arrName.indexOf(needle, indexFrom);
```

## Description
The `indexOf()` method returns the first index at which a given element can be found in the array or -1 if it is not present.  
The first parameter, *needle*, is the element to search for.  
The second parameter, *indexFrom*, is the index of the array to search from.

## Examples
```javascript
var a = [2, 9, 9]; 
a.indexOf(2); // 0 
a.indexOf(7); // -1

if (a.indexOf(7) === -1) {
  // element doesn't exist in array
}
```
How can we test if an element DOES exist in the array?

# Classwork
1. [Stringify Two Arrays](https://github.com/AryanJ-NYC/web-curriculum/blob/master/lessons/javascript-fundamentals/objects-and-arrays/array-methods-exercises.md#q7-stringify-two-arrays)
2. [Remove from Array](https://github.com/AryanJ-NYC/web-curriculum/blob/master/lessons/javascript-fundamentals/objects-and-arrays/array-methods-exercises.md#q10-remove-from-array)
3. [Array String Plus](https://github.com/AryanJ-NYC/web-curriculum/blob/master/lessons/javascript-fundamentals/objects-and-arrays/array-methods-exercises.md#q11-array-string-plus)
4. [Array Last to First](https://github.com/AryanJ-NYC/web-curriculum/blob/master/lessons/javascript-fundamentals/objects-and-arrays/array-methods-exercises.md#q12-array-last-to-first)
