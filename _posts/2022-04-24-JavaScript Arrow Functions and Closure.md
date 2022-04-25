# Closure

1) A closure is a function having access to the parent scope, even after the parent function has closed.
2) Closures are a property of JavaScript functions 
3) Call function in different scope than where function was original defined

For example: 

```javascript
const add = (function () {
  let counter = 0;
  return function () {counter += 1; return counter}
})();

add();
add();
add();
```
```
1
2
3
```

- The variable add is assigned to the return value of a self-invoking function. 
- The self-invoking function only runs once. It sets the counter to zero (0), and returns a function expression.
- This way add becomes a function. The "wonderful" part is that it can access the counter in the parent scope.
- This is called a JavaScript closure. It makes it possible for a function to have "private" variables.
- The counter is protected by the scope of the anonymous function, and can only be changed using the add function.

# Arrow functions

- To create an arrow function with don't need a name nor the function keyword but only a `=>` after the parameters that points towards the body
- `return` is implicit, so the arrow functions will return the evaluation of the body
- For example:
```javascript
//These 2 functions are equivalent

const username = 'john';
function capitalizeName(name) {
  return `${name.charAt(0).toUpperCase()}${name.slice(1)}`;  
}

const username = 'john';
const capitalize = name => `${name.charAt(0).toUpperCase()}${name.slice(1)}`;
 console.log(capitalize(username));
 ```
