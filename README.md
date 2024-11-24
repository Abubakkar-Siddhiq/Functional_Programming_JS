# Functional Programming in JS

## Functions

### Function Statement / Function Declaration

This way of creating a function is called Function Statement.

```javascript
function statement() {
  console.log("I'm a Function Statement.");
}
```

### Function Expression

Assigning a function to a variable is called Function Expression.

```javascript
var expression = function () {
  console.log("I'm a Function Expression.");
};
```

### Difference between Function Statement and Function Expression

- The difference is hoisting.
- We can call the Function Statement before declaring it.
- But, Doing that in Function Expression will throw an Error. Coz, We called it before creating the function.
- Function Expressions are treated the same as Variables.

### Anonymous Functions.

- They dont have their own identity.
- function () { } -> Will throw an Error stating "Function statements require a function name".
- Can be used in _Function Expressions_ and _Closures_ Etc.,

### Uses of Anonymous Functions:

- When function are used as values. i.e., Function Expressions.
- Callback Functions. Which are passed as an Argument in other Functions.
- Immediately Invoked Function Expressions (IIFE). Eg:

```javascript
(function () {
  console.log("I will run immidiately");
})();
```

- Event Handlers. Eg:

```javascript
.addEventListener("click", function() {
    alert("Button clicked!")
    });
```

- Higher Order Functions.
- Creating Closures.

### Named Function Expression.

- A named function expression allows you to define a function with a name that is only accessible within the function itself.
- Unlike regular Functions, Named Functions are not hoisted and only accessible within scope.
- Eg:

```javascript
const fun = function namedFn() {
  console.log("I'm a named function");
};
```

### Diff. between Parameters & Arguments

```javascript
function hi(greet, name) {
  // greet and name are paramenters.
  console.log(greet + "! " + name);
}
hi("Hi", "Siddhiq"); // The values passed to the Function's Parameters are Arguments.
```

### First-Class Functions.

- First Class Functions are the First Class Citizens. Meaning that they enjoy all the rights and privileges of any other variable or object in the language.
- First Class Functions can be passed as Arguments, Returned, and Stored as Variables.
- They are treated as Objects.
