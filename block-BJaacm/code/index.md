```js
let user = {
  name: 'Arya',
  sibling: ['Robb', 'Ryan', 'John'],
};
let allBrothers = ['Robb', 'Ryan', 'John'];
let brothersCopy = user.sibling;
let usename = user.name;
let newUser = user;
```

1. Memory representation

- Create the memory representation of the above snippet on notebook.
- Take a photo/screenshot and add it to the folder `code`

<!-- To add this image here use ![name](./hello.jpg) -->

2. Answer the following with reason:

- `user == newUser;` // output and reason // true, user and newUser are pointing at the same memory address
- `user === newUser;` // true, they are pointng to the same memory address
- `user.name === newUser.name;`// true ""
- `user.name == newUser.name;` // true ""
- `user.sibling == newUser.sibling;` // true ""
- `user.sibling === newUser.sibling;` // true ""
- `user.sibling == allBrothers;` // false the variables data are saved in different memory addresses
- `user.sibling === allBrothers;` // false, ''
- `brothersCopy === allBrothers;` // false, both are pointing to different memory addresses
- `brothersCopy == allBrothers;` // false, ''
- `brothersCopy == user.sibling;` // true. ''same address
- `brothersCopy === user.sibling;` // true ''
- `brothersCopy[0] === user.sibling[0];` // true, ''
- `brothersCopy[1] === user.sibling[1];` // true, ''
- `user.sibling[1] === newUser.sibling[1];` // true , ''
