# :clipboard: javascript-cheatsheet
Cheatsheet for Javascript Syntax and Functionalities

## Data Types
* ### Primitive
  * Boolean
  * Null
  * Undefined
  * Number
  * BigInt
  * String
  * Symbol
  
* ### Objects
  * Array
  * Typed Array
  * Map
  * Set
  * Date
  * etc.
  
### Examples:
```javascript
let myString = "string"; // String

let myNum = 123; // Number

let myBool = true; // Boolean

let myObject = { // Object
  property: "a property",
  method: function (){
    return "There is a method and " + this.property + " within this object.";
  }
};

let myArray = ['a', 'b', 'c', 1, 2, 3]; // Array
```
## Declaration and Initialization of Variables

* const
* let
* var
* *omission of keyword*

### const
This keyword is used to identify a constant variable thats type and immediate data can not be changed.

Example:
```javascript
const API_KEY = "1234567890";

API_KEY = "9999999999";  // Creates an error as const variables cannot change value
```

### let
This keyword creates a variable thats contents can be changed.

Example:
```javascript
let name = "Bob";

name = "Bobby"; // Can change contents with let keyword
```
### var
This keyword is the old syntax to create a variable that can be changed but let should be used instead since variables initialized with var can be seen outside of code blocks that it was declared within and certain other scopes.

Example:
```javascript
{
  var foo = "Fooo"
  let bar = "Barr";
}

console.log(foo); // Fooo
console.log(bar); // ReferenceError
```

### *omission of keyword*
Initalization a variable without a keyword creates a global variable that is apart of the global object of the environment and therefore should not be done unless intended.

Example:
```javascript
globalVar = "DO NOT DO THIS";
```
