# Operators & Expressions in JS

# Operators

JavaScript operators can be categorized into two main categories i.e., Unary and Binary operators. Unary takes only one operand whereas binary takes two.

## Binary Operators

Binary operators can further be divided into following types:

## Arithmetic Operators (+, -, *, /
+,−,∗,/
)

```javascript
//Arithmetic Operators
console.log("****Arithmetic Operators****\n")
console.log("2 + 3 = " + (2 + 3))
console.log("2 - 3 = " + (2 - 3))
console.log("2 * 3 = " + (2 * 3))
console.log("6 / 3 = " + (6 / 3))
console.log("7 / 3 = " + (7 / 3))
```

## Assignment Operators (=, +=, -=, *=, /=)

```javascript
//Assignment Operators
console.log("\n****Assignment Operators****\n")
var x = 3;
console.log("x = " + x)
console.log("x += 1 gives x = " + (x+=1)) // adds 1 = value of x=4
console.log("x -= 1 gives x = " + (x-=1)) // subtracts 1 = value of x=3
console.log("x *= 3 gives x = " + (x*=3)) // multiplies 3 with x = value of x=9
console.log("x /= 3 gives x = " + (x/=3)) // Divides 3 with x = value of x=3
```

## Logical Operators (&&, ||, ! )

```javascript
//Logical Operators
console.log("\n****Logical Operators****\n")
console.log("1 OR 1 = " + (1 || 1)) // 1 OR 1
console.log("1 OR 0 = " + (1 || 0)) // 1 OR 0
console.log("0 OR 0 = " + (0 || 0)) // 0 OR 0
console.log("1 AND 1 = " + (1 && 1)) // 1 AND 1
console.log("1 AND 0 = " + (1 && 0)) // 1 AND 0
console.log("0 AND 0 = " + (0 && 0)) // 0 AND 0
console.log(!true)  // NOT TRUE
console.log(!1)     // NOT TRUE
```

## Comma Operator ( , ): 
The Comma operator evaluates each operand from left to right and returns the value of right most operand.

```javascript
//Comma operator
console.log("\n****Comma Operator****")
var a = 4;
a = (a++, a);
console.log("The value for expression with comma operator is: " + a) //returns 5
```

## Comparison Operators (<, >, ==, !=, <,>,==,!=)
```javascript
//Comparison operators
console.log("\n****Comparison Operators****")
console.log(1 > 2) //false
console.log(1 < 2) //true
console.log(1 == 1) //true
console.log(1 != 1) //false
```

## Bitwise Operators (&, |, ^)

```javascript
//Bitwise Operator
console.log("\n****Bitwise Operators****")
console.log("Bitwise AND of 5 and 1: " + (5 & 1)) //returns 1
console.log("Bitwise OR of 5 and 1: " + (5 | 1)) // returns 5 
console.log("Bitwise XOR of 5 and 1: " + (5 ^ 1)) //returns 4
```

## String Operators (+)
```javascript
//String Operator
console.log("\n****String Operator****")
console.log("Concatenation" + " (+)" + " operator in action")
```

## Conditional Operators (? :)

```javascript
//Conditional Operator
console.log("\n ****Conditional Operator****")
var num_of_months = 13
var ans = (num_of_months > 12) ? "Invalid" : "Valid"
console.log(ans) //Returns Invalid
```

## Unary Operators

- typeof: Returns the type of the given operand
- delete: Deletes an object, object’s attribute or an instance in an array
- void: Specifies that an expression does not return anything
- Increment Operators : ++, --

## Interview Question 
**What is the difference between == and ===**

*The operator === is commonly referred as Deep Equals in JavaScript. The only difference between double equals == and deep equals is that the former does not perform type comparison but in fact, converts the type of one of the operands to make their types same. Deep equals, on the other hand, returns false if both types are not the same.*

See the example given below for better understanding:
```javascript
console.log(1 == 1); //returns true
console.log('1' == 1); //returns true
console.log(1 === 1); //returns true
console.log('1' === 1); //returns false
```

# Expressions
Anything that evaluates to a value is called an expression. Some of the basic expressions and keywords used in JavaScript are mentioned below:

this: points to the current object
super: calls methods on an object’s parent, for example, call parent’s constructor
function: used to define a function
function*: used to define a generator function
async function: used to define an async function

