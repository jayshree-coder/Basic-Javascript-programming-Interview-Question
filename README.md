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
