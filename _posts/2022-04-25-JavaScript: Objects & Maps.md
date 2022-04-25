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
# Merging Objects
- We can use Object.assign(object, newObject) to merge information while preserving the defaults
- Since objecta are passed by reference instead of value, we don't want to merge new values into the original object but a new one
- We are now able to establish common default properties of any objects through mergins and to non-destructeveily updte properties


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

console.log(Object.assign({}, user, newUser, { verified: false }));
```
```javascript
{name: "", username: "ReedBarger", phoneNumber: "", email: "reed@gmail.com", password: "mypassword", verified: false}
```

- We can also gain more control of the new object by specifying directly the properties we want
- To avoid creating nested objects we can spread in the properties with the operator `...`

```javascript
const createdUser = { ...user, ...newUser, verified: false };
```

# Maps
- Maps can have any primitive type as a key
- Maps preserve insertion order
- WeakMap do the same but it is optimized for garbage collections and memory optimization
- `map1.set('key', 'value');` will add value pairs and `map1.size` will return the number of pair in the map

```javascript
const user1 = { name: "john" }
const user2 = { name: "mary" }

const secretKey1 = "asldjfalskdjf";
const secretKey2 = "alksdjfakjsdf";

const secretKeyMap = new WeakMap([
  [user1, secretKey1],
  [user2, secretKey2]  
]);

const key = secretKeyMap.get(user1);
console.log(key);

const user = {
  name: "john",
  verified: true  
};

const userMap = new Map([
  ["name", "john"],
  ["verified", true]  
]);

console.log(userMap.size);
```
