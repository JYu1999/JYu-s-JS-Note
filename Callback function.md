Callback Function is a [[JS Function]] passed as an argument to another function
This technique allows a function to call another function
A callback function can run after another function has finished ^6533fb
# Example
Using a callback, you could call the calculator function (`myCalculator`) with a callback (`myCallback`), and let the calculator function run the callback after the calculation is finished:
```js
function myDisplayer(some) {
 console.log(some); 
}

function myCalculator(num1, num2, myCallback) {
  let sum = num1 + num2;
  myCallback(sum);
}

myCalculator(5, 5, myDisplayer);
```

> [!note]
> When you pass a function as an argument, remember not to use parenthesis.
> Right: myCalculator(5, 5, myDisplayer);
> Wrong: ~~myCalculator(5, 5, myDisplayer())~~;


```js
// Create an Array
const myNumbers = [4, 1, -20, -7, 5, 9, -6];

// Call removeNeg with a callback
const posNumbers = removeNeg(myNumbers, (x) => x >= 0);

// Display Result
console.log(posNumbers);

// Keep only positive numbers
function removeNeg(numbers, callback) {
  const myArray = [];
  for (const x of numbers) {
    if (callback(x)) {
      myArray.push(x);
    }
  }
  return myArray;
}
```
