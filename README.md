# Lecture 3
# TREE EMPORTANT TOPIC

## Scope - Hoisting - TDZ
### What is Scope in JavaScript ?
Scope in JavaScript refers to the accessibility and lifetime of variables, functions, and objects in different parts of the code. It determines where variables can be accessed or modified.
```
           Types of Scope in JavaScript
              |                  | 
         Global Scope          Local Scope
                                |       | 
                     Function Scope    Block Scope
```

# The role of Global Scope

Global Scope : Global scope is the widest
scope available. Variables declared in global
scope are accessible from anywhere in your
code, whether it's inside functions, conditional
statements, loops, or other blocks of code

Variables declared in global scope are
accessible everywhere

The global execution context is the primary context that is created
whenever JavaScript code is loaded for execution. It represents the base
scope in which program-wide variables, functions, and objects operate.



The global context contains global variables, functions, and other objects
that are accessible throughout the program.

## Example:   
```
var globalVar = "I am a global variable";

function displayGlobal() {
  console.log(globalVar); // Accessible inside function
}

displayGlobal();
console.log(globalVar); // Accessible outside function too

```
# Function Scope
Function scope in JavaScript refers to the scope of variables and functions that are defined
within a function. Variables and functions declared with the var keyword have function
scope.

Variables declared inside a function are accessible only within that function and any nested
functions. They are not accessible outside of the function in which they are defined. This
means that variables declared within a function cannot be accessed before their
declaration or outside of the function
## Example:
```
function testScope() {
  var a = "var inside function";
  let b = "let inside function";
  const c = "const inside function";

  console.log(a, b, c); // ✅ All accessible inside function
}

testScope();
console.log(a); // ❌ Error: a is not defined
console.log(b); // ❌ Error: b is not defined
console.log(c); // ❌ Error: c is not defined
```
# Block Scope
Block scope in JavaScript refers to the scope of variables and functions that are defined
within a block of code, such as within a pair of curly braces {}. Variables and functions
declared with let and const keywords have block scope.Variables declared inside a function
are accessible only within that function and any nested functions. They are not accessible
outside of the function in which they are defined. This means that variables declared within a
function cannot be accessed before their declaration or outside of the function.
## Example:
```
{
  let blockVar = "I'm inside a block";
  console.log(blockVar); // ✅ Accessible inside block
}

console.log(blockVar); // ❌ Error: blockVar is not defined

```

# what is Hoisting ?
Hoisting is a JavaScript mechanism where variables and function declarations are moved to the
top of their scope before code execution.

Hoisting in JavaScript is a behavior in which a function or a variable can be used before
declaration.
## Example:
```
console.log(a); // ❓ Output: undefined (Hoisted but not initialized)
var a = 10;
console.log(a); // ✅ Output: 10

```

# Function (declaration) - Hoisting
In JavaScript, function declarations are fully
hoisted. This means that both the function's
name and its definition are moved to the top
of their scope, making the function available
to be called anywhere in that scope, even
before its actual declaration in the code.

## Example:
```
sayHello(); // ✅ Works!

function sayHello() {
  console.log("Hello!");
}

```
# TDZ - Temporal dead zone let and const

TDZ : Is the term to describe the state where
variables are un-reachable. They are in
scope, but they aren't declared.

The let and const variables exist in the TDZ
from the start of their enclosing scope until
they are declared.

Relatively simply, always make sure you
define your lets and consts at the top of your
scope.

# Thank you be Happy and smile 😁
