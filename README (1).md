# 10 JavaScript One-Liners That Will Blow Your Mind

## 1. Reverse a String
```js
const reverse = str => str.split('').reverse().join('');
```
How it works:  
- `split("")` converts string into an array  
- `reverse()` reverses the array  
- `join("")` joins back into a string

## 2. Check if a String is a Palindrome
```js
const isPalindrome = str => str === str.split('').reverse().join('');
```
Compares the original string with its reversed version.

## 3. Remove Duplicates from an Array
```js
const unique = arr => [...new Set(arr)];
```
Uses Set to store only unique values.

## 4. Generate a Random Hex Color
```js
const randomColor = () => '#' + Math.floor(Math.random()*16777215).toString(16);
```
Generates a random color using Math.random().

## 5. Find the Maximum Value in an Array
```js
const max = arr => Math.max(...arr);
```
Uses the spread operator (`...`) with Math.max().

## 6. Convert a Number to Binary
```js
const toBinary = num => num.toString(2);
```
Converts number to binary using `.toString(2)`.

## 7. Sum of an Array
```js
const sum = arr => arr.reduce((a, b) => a + b, 0);
```
Uses `reduce()` to add all elements.

## 8. Capitalize the First Letter of a String
```js
const capitalize = str => str.charAt(0).toUpperCase() + str.slice(1);
```
Converts first character to uppercase.

## 9. Shuffle an Array (Fisher-Yates Algorithm)
```js
const shuffle = arr => arr.sort(() => Math.random() - 0.5);
```
Uses `Math.random()` inside `sort()` for randomization.

## 10. Get the Current Date in YYYY-MM-DD Format
```js
const currentDate = () => new Date().toISOString().split('T')[0];
```
Uses `toISOString()` and `split()` to format the date.
