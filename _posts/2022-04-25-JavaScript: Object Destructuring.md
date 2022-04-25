# Property Access with Destructuring

- By wrapping properties of an object with curly braces we can pull whatever properties of objects and make them variables

```javascript
const user = {
  name: "Reed",
  username: "Reedbarger",
  email: "reed@gmail.com",
  details: {
    title: "Programmer"  
  }  
};

// const { title } = user.details
const { name, details: { title} } = user;

function displayUserBio() {
  console.log(`${name} is a ${title}`); 
}

displayUserBio()

// const { username, email } = user;

// function displayUser() {
//   console.log(`username: ${username}, email: ${email}`);  
// }

// displayUser()
```
```
›Reed is a Programmer
```
