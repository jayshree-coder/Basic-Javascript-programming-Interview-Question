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
    <p>By using two methods together and creating a deep clone, I can serialize the object to a JSON string. I would then parse it back into a new object, thereby removing any reference to the original object. </p>
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

