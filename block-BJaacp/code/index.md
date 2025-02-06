1. What will be the output and explain the reason.

```js
let obj = { name: 'Arya' };
obj = { surname: 'Stark' };
let newObj = { name: 'Arya' };
let user = obj;
let arr = ['Hi'];
let arr2 = arr;
```

Answer the following with reason after going through the above code:

- `[10] === [10]`
- What is the value of obj? // answer
- `obj == newObj` //False, obj was reassigned siwth surname key.
- `obj === newObj` //false, ''
- `user === newObj` // false, user equals obj which has a surname key.
- `user == newObj` // false, ''
- `user == obj` // true, user and obj have same keys and values and are pointing to the same address.
- `arr == arr2` // true, the have the same array. They are pointing to the same address.
- `arr === arr2` // true, they are pointing to the same address

2. What's will be the value of `person1` and `person2` ? Explain with reason. Draw the memory representation diagram.

<!-- To add this image here use ![name](./hello.jpg) -->

![Hello]./hello.jpg

```js
function personDetails(person) {
  person.age = 25;
  person = { name: 'John', age: 50 };
  return person;
}
var person1 = { name: 'Alex', age: 30 };
var person2 = personDetails(person1);
console.log(person1); //In the function the property age was changed to 25. Howver, when the object person was being changed completely it created a new memory address and was not pointing to the original memory addressof person1. 
console.log(person2); // Person2 just shows the returned object from the function.
```



3. What will be the output of the below code:

```js
var brothers = ['Bran', 'John'];
var user = {
  name: 'Sansa',
};
user.brothers = brothers;
brothers.push('Robb');
console.log(user.brothers === brothers); //True , they are both pointing to the same memory address
console.log(user.brothers.length === brothers.length); //true, they are pointing to the same memory address and thus have the same array length.
```
