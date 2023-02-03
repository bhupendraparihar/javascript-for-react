# Function Declaration in JavaScript

A function is a piece of code which is defined only once but can be called a countless number of times. 

A JavaScript function comprises several components which affect its behavior. A typical JavaScript function has the following components:

- the function keyword
- the name
- the parameter(s)
- the returned value
- the return type
- the context this


Did you know? In JavaScript, functions are actually objects. Just - like any typical object, they have attributes and methods too. The only thing that differentiates them from objects is that they can be called

## What’s the difference between Named and Anonymous function?
The only difference is that Anonymous Functions are declared at runtime, means they are defined and called at the same time. The reason why they are called Anonymous is that they are not given a proper name before compilation. A typical way to declare a function in JavaScript is:

```javascript
function myFunction()
{
  console.log("Hello! I'm a named function!");
}

myFunction();
```
Now here’s how an anonymous function is dynamically declared:

```javascript
var myFunction = function()
{
  console.log("Hello! I'm an Anonymous function");
}

myFunction();
```

## Ways to Declare JavaScript Function
The six different methods which are used in JavaScript to declare a function.

- Function Declaration
```javascript
function add(a, b) {
    return a + b;
}
```

- Function Expression
```javascript
const add = function(a,b) {
    return a + b;
}
```

- Arrow Function
```javascript
const add = (a,b) => a + b;
```

- Function Constructor
```javascript
const add = new Function('a', 'b', 'return a + b');
```

## Coding Challange
Write a function expression(arrow function) to find hypotenuse of the right triange using pythogorus theorem. Your function should take perpendicular and base as input and return hypotenuse as output.

### Solution
```javascript
const cube = n => n^3;

console.log(cube(5)); // 125
```

## Arrow function in React
```javascript
// JavaScript ES5 function
function getGreetingFunc() {
  return 'Welcome to JavaScript';
}

// JavaScript ES6 arrow function with body
const getGreetingArrow1 = () => {
  return 'Welcome to JavaScript';
}

// JavaScript ES6 arrow function without body and implicit return
const getGreetingArrow2 = () =>
  'Welcome to JavaScript';

console.log(getGreetingFunc());
console.log(getGreetingArrow1());
console.log(getGreetingArrow2());
```

Another Example, **Print all the students who is present**
```javascript
const students = [
  { ID: 1, present: true},
  { ID: 2, present: true},
  { ID: 3, present: false}, 
];

const presentStudents = students.filter(function(student){return student.present;});
console.log(presentStudents);
```
 Use Arrow function here
 ```javascript
const presentStudents = students.filter(student => student.present);
console.log(presentStudents);
```

## Rules of thumb:
While writing an arrow function or transforming an existing function into arrow function, you must keep these points in mind:

- If there is only one statement inside function body then you can omit return keyword as well the curly braces
- Omit the function keyword in the beginning
- You can also get rid of parameter parentheses if you only have one parameter

### Challenge - Convert the below function to arrow function
```javascript
function square(n){
  return n*n;
}
```

### Print all the arguments passed to a function
```javascript
function add() {
  // Arguments are array like object, you can you normal for-loop or for-of loop to access it
  console.log(arguments);
}
```

### Write a function to add N numbers passed as an arguements
```javascript
function add() {
  let sum = 0;
  for(let n of arguments) {
    sum += n;
  }
  return sum;
}

```
