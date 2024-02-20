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
###