All section headers are linked to the appropriate documentation.  Use the links for more information.
# [Slice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/slice)
```javascript
var arr = ['a', 'b', 'c', 'd'];
var copy = arr.slice(); // ['a', 'b', 'c', 'd']
var sliced = arr.slice(0, 2); // [a, b]
```

# [Splice](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/splice)
```javascript
var myFish = ['angel', 'clown', 'mandarin', 'sturgeon'];

myFish.splice(2, 0, 'drum'); // insert 'drum' at 2-index position
// myFish is ["angel", "clown", "drum", "mandarin", "sturgeon"]

myFish.splice(2, 1); // remove 1 item at 2-index position (that is, "drum")
// myFish is ["angel", "clown", "mandarin", "sturgeon"]
```

# [Push](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push?v=example)
```javascript
var numbers = [1, 2, 3];
numbers.push(4);

console.log(numbers); // [1, 2, 3, 4]

numbers.push(5, 6, 7);

console.log(numbers); // [1, 2, 3, 4, 5, 6, 7]
```

# [Unshift](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift)
```javascript
var a = [1, 2, 3];
a.unshift(4, 5);

console.log(a); // [4, 5, 1, 2, 3]
```

# [Pop](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop)
```javascript
var a = [1, 2, 3];
a.pop(); // 3

console.log(a); // [1, 2]
```

# [Shift](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift)
```javascript
var a = [1, 2, 3];
var b = a.shift();

console.log(a); // [2, 3]
console.log(b); // 1
```

# [Concat](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/concat)
```javascript
var arr1 = ['a', 'b', 'c'];
var arr2 = ['d', 'e', 'f'];

var arr3 = arr1.concat(arr2); // [ "a", "b", "c", "d", "e", "f" ]
```

# [Join](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/join)
```javascript
var a = ['Wind', 'Rain', 'Fire'];
a.join();    // 'Wind,Rain,Fire'
a.join('-'); // 'Wind-Rain-Fire'
```

# [IndexOf](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf)
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
1. [Stringify Two Arrays](https://github.com/C4Q/web-curriculum/blob/master/lessons/javascript-fundamentals/objects-and-arrays/array-methods-exercises.md#q7-stringify-two-arrays)
2. [Remove from Array](https://github.com/C4Q/web-curriculum/blob/master/lessons/javascript-fundamentals/objects-and-arrays/array-methods-exercises.md#q10-remove-from-array)
3. [Array String Plus](https://github.com/C4Q/web-curriculum/blob/master/lessons/javascript-fundamentals/objects-and-arrays/array-methods-exercises.md#q11-array-string-plus)
4. [Array Last to First](https://github.com/C4Q/web-curriculum/blob/master/lessons/javascript-fundamentals/objects-and-arrays/array-methods-exercises.md#q12-array-last-to-first)
