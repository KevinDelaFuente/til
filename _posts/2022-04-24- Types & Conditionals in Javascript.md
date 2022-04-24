# If statements

- Basic Structure of `if` control flow

```javascript
// if statements - evaluate boolean values
// const prefersDarkMode = true;
// const prefersSolarizedMode = true;
const colorMode = 'dark';

if (colorMode === 'solarized') {
   console.log('solarized mode set!'); 
   document.body.style.background = 'palegoldenrod';
} else if (colorMode === 'dark') {
  console.log('dark mode set!');  
  document.body.style.background = 'black';
} else {    
  console.log('light mode set!');
  document.body.style.background = 'ghostwhite';
}
```
- Can be replaced with `switch`, where conditionals are replaced by cases and else with default :

```javascript
const colorMode = 'dark';

switch (colorMode) {
  case "solarized":
   console.log('solarized mode set!'); 
   document.body.style.background = 'palegoldenrod';
  case 'dark':
    console.log('dark mode set!');  
    document.body.style.background = 'black';
  default:  
    console.log('light mode set!');
    document.body.style.background = 'ghostwhite';
}
```
