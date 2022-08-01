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
  var foo = "Fooo";
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
## Conditionals
* boolean values
* boolean expressions
* comparison operators
* logical operators
* conditionals

### boolean values
Boolean values are and important data type within javascript and are used in evaluation of boolean expressions and conditionals

Example:
```javascript
var myBool = true;
console.log(typeof myBool); // boolean

myBool = false;
console.log(typeof myBool); // boolean
```

### boolean expressions
Boolean expressions are expressions that are evaluated and return either a value of true or false in order to show a relationship or to be used in conditionals

Example:
```javascript
console.log(5 === 5); // true
console.log(10 === 5); // false

console.log(false == "false"); //false
```

### comparison operators
JavaScript has multiple types of operators that allow for comparison of variables of raw values that would signify the realationship between the operators by returning true or false

Example:
```javascript
// (Note: Loose equal and not equal comparisons have some automatic type conversion so in som cases comparison of different types can return true)

// Loose Equal (loosely checks if values are equal to one another)
console.log(20 == 20); // true
console.log(20 == 33); // false

// Loose Not Equal (loosely checks if values are not equal to one another)
console.log(45 != 15); // true
console.log(24 != 24); // false

(Note: Strict equal and not equal comparisons will always honor original type when comparing)
// Strict Equal (strictly checks if values are equal to one another)
console.log("cat" === "cat"); // true
console.log("cat" === "dog"); // false

// Strict Not Equal (strictly checks if values are not equal to one another)
console.log("turtle" !== "frog"); // true
console.log("turtle" !== "turtle");

// (Note: Greater than and less than comparisons can still compare values that aren't number types)
// Greater Than (checks if the first operand is greater than the second operand)
console.log(35 > 15); // true
console.log(11 > 12); // false

// Less Than (checks if the first operand is less than the second operand)
console.log(91 < 102); // true
console.log(3 < 2); // false

// Greater Than or Equal To (checks if the first operand is greater than or equal to the second operand)
console.log(22 >= 21); // true
console.log(22 >= 22); // true
console.log(7 >= 19); // false

// Less Than or Equal To (checks if the first operand is less than or equal to the second operand)
console.log(26 <= 94); // true
console.log(26 <= 26); // true
console.log(63 <= 57); // false
```

### logical operators
logical operators allow for more complex boolean expressions that use operators that take multiple boolean expressions and evaluate them as a larger one
 
 Example:
 ```javascript
 // Logical AND (&&)
 console.log("apple" === "apple" && 40 > 30); // true
 console.log(91 >= 203 && true); // false
 
// Logical OR (||)
console.log(72 < 98 || true === false); // true
console.log(false !== false || "cat" === "dog"); // false

// Logical NOT (!)
console.log(!(85 < 37)); // true
console.log(!("joe" === "joe")); // false
 ```
