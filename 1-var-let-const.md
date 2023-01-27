## Defining variables in JavaScript

In JavaScript you can define variable by using three keywords
```javascript
var a = 10;
let b = 15;
const c = 20;
```
They all the valid declartion, so the question is when to use what. let and const came into existence with ES6(EcmaScript2015). The key differnce is there scope. 

Let's say you define a variable message:
```javascript
const message = 'Hello';
console.log(message); // 'Hello'
```
Then, you could easily log this variable in the next line after the declaration. No questions here.

Now, let's move the declaration of message inside of an if code block:
```javascript
if (true) {
  const message = 'Hello';
}
console.log(message); // ReferenceError: message is not defined
```
This time, when trying to log the variable, JavaScript throws ReferenceError: message is not defined.

Why does it happen?

The if code block creates a scope for message variable. And message variable can be accessed only within this scope.

## JavaScript Scope

At a higher level, the accessibility of variables is limited by the scope where they're created. You are free to access the variable defined within its scope. But outside of its scope, the variable is inaccessible.

Now, let's put down a general definition of scope:

*The scope is a policy that manages the accessibility of variables.*

## The Scope of var, let and const

- var: Function in which the variable is declared
- let: Block in which the variable is declared
- const: Block in which the variable is declared

**Block scopes are what you get when you use if statements, for statements or write code inside curly brackets.**

Example
```javascript
function foo(){
  for (var i=0; i<5 ; i++){
    console.log(i);
  }
  console.log(i);
}

foo();
```
Run this code, and you will see the last value of i is 5.

Now change the var to let, and you will get the error ReferenceError: i is not defined. This shows that i is only accessible within the curly brackets. This is Block Scope. where as variable declared with var, can be accessed anywhere inside the function, this is called Function Scope.


## Rules of Thumb:
- Don’t use var, because let and const is more specific
- Default to const, because it cannot be re-assigned or re-declared
- Use let when you want to re-assign the variable in future
- Always prefer using let over var and const over let

