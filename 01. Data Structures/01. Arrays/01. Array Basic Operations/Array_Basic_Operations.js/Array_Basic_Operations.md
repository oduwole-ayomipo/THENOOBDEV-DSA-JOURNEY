### Array Overview:

In JavaScript,

    - an array is a data structure that allows us to store and manipulate a collection of values.

    - An array can contain different data type ranging from strings, number, and even another array itself.

    - Array variables, we can store several pieces of data in one place.

```js
const rice = ["white rice", "jollof rice", "ofada rice"];
const wordsAndNumber = [1, "one", 2, "two", 3, "three"];
```

### Accessing Elements:

    - Elements of an arraay can be accessed using it's index.

    - Just like stings, arrays use zero-based indexing, so the first element in an array has an index of 0.

```js
const rice = ["white rice", "jollof rice", "ofada rice"];
console.log(array[0]);
const myFav = array[1];

// The console.log(array[0]) prints white rice, and myFav has the value jollof rice.
```

### Updating Elements:

    - we can update the value of an element in an array by assigning a new value to its corresponding index:

```js
let rice = ["white rice", "jollof rice", "ofada rice"];
rice[1] = "coconut rice";

// Updates the second element to coconut rice
```

### Finding the Length:

    - we can find the number of elements in an array using the length property:

```js
let myArray = [1, 2, 3, 4, 5];
let arrayLength = myArray.length;

// Returns 5
```

### Finding the Nth element in an array:

    - suppose we have no idea how long the array is, but we uwish to get the 3rd to the last element

```js
let rice = [
  "white rice",
  "jollof rice",
  "ofada rice",
  "coconut rice",
  "fried rice",
];
let thirdToLastElementOfRice = rice[rice.length - 3];

// Updates the second element to coconut rice
```

### Insertion

    - we can insert elements to the end of an array using the push() method:

```js
let myArray = [1, 2, 3];
myArray.push(4);

// Inserts 4 to the end of the array
```

    - we can also add elements to the beginning of an array using the unshift() method:

```js
let rice = ["white rice", "jollof rice", "ofada rice"];
myArray.unshift("fried rice");

// Inserts fried rice to the beginning of the array
```

    - To remove the last element from an array, we can use the pop() method:

```js
let rice = ["white rice", "jollof rice", "ofada rice"];
myArray.pop();

// Removes the last element (ofada rice in this case)
```

    - To remove the first element from an array, you can use the shift() method:

```js
let myArray = [1, 2, 3, 4];
myArray.shift();

// Removes the first element (1 in this case)
```

#### That's all for now, next we are going to look at traversals and solve some hackerrank challenges under arrays!
