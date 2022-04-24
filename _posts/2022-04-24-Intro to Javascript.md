
# Variables and Strings



## Strict Mode
- Javascript can be run un two ways:
 1) sloppy "normal" mode - default in scripts
 2) strict mode - throws more errors, prevents pitfalls of the language
- We can switch to strict mode by writing `"use strict";` at the top of the code
- By using strict mode we can prevent ourselves from overwiriting global objects and mutating existing properties 
- _Hoisting_ is the ability in js to access a variable before it is created
  - To avoid this issue we can use `let` and `const` as they will throw unitiliazed error   
