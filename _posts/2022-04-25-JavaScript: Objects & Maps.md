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
# Mergin Objects
- We can use Object.assign(object, newObject) to merge information while preserving the defaults
- Since objecta are passed by reference instead of value, we don't want to merge new values into the original object but a new one

```javascript
const user = {
  name: "",
  username: "",
  phoneNumber: "",
  email: "",
  password: ""  
};

const newUser = {
  username: "ReedBarger",
  email: "reed@gmail.com",
  password: "mypassword"  
};

console.log(Object.assign({}, user, newUser));
```
```
{name: "", username: "ReedBarger", phoneNumber: "", email: "reed@gmail.com", password: "mypassword"}
```
