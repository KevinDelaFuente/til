# Coercion of Data Types

- JS has an implicit coercion of data types for conditionals: booleans. Therefore even non-boolean values will be coerced into it, creating _truthy_ and _falsy_ values
- _falsy_      
  1) false
  2) 0
  3) ''
  4) null
  5) undefined
  6) NaN
- _truthy_
  - everything else
- Tips to avoid issues with these types:
  1) Avoid direct comparisons in conditionals

```javascript
const username = '';

if (!username) {
  console.log('no user');
}

>no user
```

  2) Use triple equals === (strict equals operator)

```
if (null === undefined) {
  console.log('equals');
} else {
  console.log('not equals');
}
```
```
>equals
```
  3) 
