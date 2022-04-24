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
```
```javascript
>no user
```

  2) Use triple equals === (strict equals operator) vs lose equals operator == that coerces

```javascript
if (null == undefined) {
  console.log('equals');
} else {
  console.log('not equals');
}
```
```javascript
>equals
```
  3) Convert to real Boolean values where needed

```javascript
if (NaN === NaN) {
    console.log('equal')
} else {
    console.log('not equals')
}
```
```javascript
>not equals
```
