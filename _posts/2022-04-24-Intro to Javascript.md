
# Intro to Javascript

## Strict Mode
- Javascript can be run un two ways:
 1) sloppy "normal" mode - default in scripts
 2) strict mode - throws more errors, prevents pitfalls of the language
- We can switch to strict mode by writing `"use strict";` at the top of the code
- By using strict mode we can prevent ourselves from overwiriting global objects and mutating existing properties 
- _Hoisting_ is the ability in js to access a variable before it is created
  - To avoid this issue we can use `let` and `const` as they will throw unitiliazed error
  - When a value is going to change, we should use `let`. It works pretty similar to var
  - When a value is not going to change, we should use `const`.  
   - const - creates restrictions that make code more readable. However keep in mind that `const` 1) must be initialized with a value, and 2) can't be reassigned after declaration  

## Block Scoping
- Variable Shadowing means that variables with the same name in a function scope will shadow global var. Nevertheless, `let` and `const` are block-scoped
```javascript
var price = 20;
var isSale = true;

if (isSale) {
  // discount price of product
  var price = 20 - 2; 
  // do something 
  console.log('sale price', price);
}

console.log('price', price);
```

```
›sale price,18
›price,18
```

## Template Literal

```javascript
let username = "Jane Doe";
let message = `Hi ${username}, how are you?`;
console.log(message);
```
