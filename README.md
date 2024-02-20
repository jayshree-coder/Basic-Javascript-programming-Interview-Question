<h1 align="center">Javascript Programming Interview Question</h1>

### Description
It is a light-weighted programming language for developing interactive web pages. It can insert dynamic text into the HTML elements. JavaScript is also known as the browser’s language.

### JavaScript Coding Interview Questions 

### Write a function that finds the second largest number in an array. 
```javascript
function findSecondLargest(arr) {
    // Sort the array in descending order
    arr.sort((a, b) => b - a);
    // Return the second element of the sorted array
    return arr[1];
}

let arrayList = [1, 5, 53, 23, 54, 56];
// Call the findSecondLargest function with arrayList as argument
console.log("Second Largest Number", findSecondLargest(arrayList))
```
### write a function that returns the average value of numbers in an array. 
```javascript
function calculateAverage(numbers) {
    let sum = 0; // Initialize a variable to hold the sum of the numbers
    
    // Loop through each number in the array
    for (let number of numbers) {
        sum += number; // Add the current number to the sum
    }
    
    // Calculate the average by dividing the sum by the number of elements in the array
    return sum / numbers.length;
}

let arrayNumberList = [1, 5, 53, 23, 54, 56];
console.log("Calculate Average", calculateAverage(arrayNumberList))

```

### Write a function that returns a new array containing only the unique elements from an input array. 

```javascript
function getUniqueElements(inputArray) {
    // Create a new Set from the inputArray, which automatically removes duplicates
    // Using the spread operator (...) to convert the Set back to an array
    return [...new Set(inputArray)];
}

let arrayList3 = [1, 5, 55, 23, 55, 55, 56];
console.log("Unique numbers:", getUniqueElements(arrayList3));

```

### Write a function function that checks if a given string is a palindrome (reads the same forwards and backwards) while ignoring whitespace and punctuation. 

```javascript
function isPalindrome(str) {
    // Clean the string by removing non-alphanumeric characters and converting to lowercase
    const cleanedStr = str.replace(/[^\w]/g, '').toLowerCase(); 
    
    // Split the cleaned string into an array of characters, reverse the array, and then join it back into a string
    const reverseString = cleanedStr.split('').reverse().join('');
    
    // Compare the original cleaned string with its reversed version to check for palindrome
    return cleanedStr === reverseString;
}

let stringsPalindrome = "Hello World";

console.log("isPalindrome", isPalindrome(stringsPalindrome));
```

### Write a function that takes an array of objects and a key, and returns a new array sorted based on the values of that key in ascending order. 

```javascript

function sortByKey(arr, key)
{
    return arr.sort((a,b)=> a[key] - b[key])
}
const data = [
    { id: 3, name: 'John', age: 30 },
    { id: 1, name: 'Alice', age: 28 },
    { id: 2, name: 'Bob', age: 21 }
  ];
  
  console.log("sort by Key", sortByKey(data, 'age'));
  
  ```
  ### Write a function deep clone function in JavaScript that creates a copy of a nested object or array without any reference to the original. 
  By using two methods together and creating a deep clone, I can serialize the object to a JSON string. I would then parse it back into a new object, thereby removing any reference to the original object.

```javascript
function deepClone(obj)
{
    return JSON.parse(JSON.stringify(obj));
}

const originalObject = {
    name: 'John',
    age: 25,
    address: {
        city: 'New York',
        country: 'USA'
    },
    hobbies: ['reading', 'coding']
};
console.log("deepclone", deepClone(originalObject));
```

### Write a function that takes two sorted arrays and merges them into a single sorted array without using any built-in sorting functions. 

```javascript

function mergeAndSortArrays(array1, array2) {
    return [...array1, ...array2].sort((a, b) => a - b);
}

const sortedArray1 = [1, 3, 5, 7];
const sortedArray2 = [2, 4, 6, 8, 10];

console.log("Merged and Sorted Array", mergeAndSortArrays(sortedArray1, sortedArray2));
```

### Write a function that flattens a nested array in JavaScript, converting it into a single-level array. 
``` javascript
function flattenNestedArrays(arrays) {
    return arrays.flat();
}

let nestedArrayMerger = [[12, 30, 40], [50, 1, 3], [70, 0, 90]];

console.log("Flattened Array", flattenNestedArrays(nestedArrayMerger));
```
### Write a function to find the factorial of a given number. 

```javascript 
function factorialNumber(num) {
    if (num === 0 || num === 1) {
        return 1;
    } else {
        return num * factorialNumber(num - 1);
    }
}

let numberToCalculateFactorial = 4;
console.log("Factorial of", numberToCalculateFactorial, ":", factorialNumber(numberToCalculateFactorial));
```

### write a function to count the occurrences of each character in the string. 

```javascript
function countCharacters(str) {
    const charCount = {};
    for (let char of str) {
        charCount[char] = (charCount[char] || 0) + 1;
    }
    return charCount;
}

let inputString = "HelloWorld";

console.log("Character Count:", countCharacters(inputString));
```
### Write a function that returns the sum of all numbers in an array.  

```javascript

function sumArray(arr) {
    return arr.reduce((total, num) => total + num, 0);
}

let arrayNumberList2 = [1, 2, 3, 4, 5];
console.log("Sum of array", sumArray(arrayNumberList2));
```

### Write a function to reverse a string without using the built-in reverse() method. 

```javascript
function reverseString(str) { 
    let reversedString = "";
    for (let i = str.length - 1; i >= 0; i--) { 
        reversedString += str[i];
    }
    return reversedString;
}

let inputString = "Hello World";
console.log("Reversed String", reverseString(inputString));
```

### write a function to count of Vowels
```javascript
function countVowels(inputString) {
    inputString = inputString.toLowerCase();

    const vowels = ['a', 'e', 'i', 'o', 'u'];

    let vowelCount = 0;

    for (let char of inputString) {
        if (vowels.includes(char)) {
            vowelCount++;
        }
    }

    return vowelCount;
}

let inputString = "hello world";

console.log("Vowel Count", countVowels(inputString));
```
### Write a function that takes an array of numbers and returns a new array with only the even numbers. 

```javascript
function getEvenNumbers(array) {
    return array.filter(num => num % 2 === 0);
}

let inputArray = [1, 2, 3, 4, 5, 6];

console.log("Even Numbers", getEvenNumbers(inputArray));
```
### Write a function that merges two arrays into a single array, alternating elements from each array. 

```javascript
function mergeArrays(array1, array2) { 
    // Create an empty array to store the merged elements from both arrays
    const mergeArray = [];
    
    // Determine the maximum length between the two input arrays
    const maxLength = Math.max(array1.length, array2.length);
    
    // Iterate through each index from 0 to the maxLength
    for (let i = 0; i < maxLength; i++) { 
        // Check if the current index is within the bounds of array1
        if (i < array1.length) {
            // If yes, push the element at the current index of array1 into mergeArray
            mergeArray.push(array1[i]);
        }
        
        // Check if the current index is within the bounds of array2
        if (i < array2.length) {
            // If yes, push the element at the current index of array2 into mergeArray
            mergeArray.push(array2[i]);
        }
    }
    
    // Return the merged array containing elements from both input arrays
    return mergeArray;
}

// Define two arrays to be merged
let arr1 = [1, 5, 55, 23, 55, 56];
let arr2 = [1, 2, 3, 4, 5];

// Call the mergeArrays function with the two arrays as arguments and log the result
console.log("Merge Array:", mergeArrays(arr1, arr2));
```