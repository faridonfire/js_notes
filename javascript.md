# Javascript

## Variables

```
// let means you can change the value of the variable later on
let id = 123;
// ✅ this is allowed
id = 432;


// const means you are not allowed to change the value of the variable later on
const id = 123;
// ❌ this is not allowed
id = 432;

// var is an old way of defining variables, you should try to avoid it
var a = 123;
```

variables

- cannot start with numbers
- cannot contain symbols
- must be at least 1 character

```
// ✅ this is allowed
let x = 1;
let _ = 1;
let x1 = 1;
// ❌ this is not allowed
let % = 1;
```

## Functions

Functions have 3 things.

- name.
- parameter list
- return value

```
// regular anonymous function
// it has no name
function () {}

// function declarations are hoisted to the top of the file
function customName () {

}

// arrow functions have no name and look like this
const var = () => {};
```

If a function has the `async` keyword in front of it, it will return a promise.
It will also have the ability to use the keyword `await` to resolve other async functions

Examples

```
async function getCalculations(){
  await wait(5000);
}
```

## Objects

Objects are intialized like this

```
const obj = {};
```

Objects can have key-values.
Keys are mostly always strings.
Values are any valid js value.

### Accessing a value in an object

```
// Dot notation
// you can only use dot notation for keys that would be valid variable names
// you can define a key with non-valid variable names but you cannot use
// dot notation when accessing that key
const obj = {
  a: 1234,
  "%": 'abcd'
};
// ✅ this is allowed
console.log(obj.a)
// ❌ this is not allowed
console.log(obj.%)


// Bracket notation
const obj = {
  a: 5123,
  "!": "ABCD"
};
// ✅ this is allowed
console.log(obj['a'])
// ✅ this is also allowed
console.log(obj['!'])
```

### Assigning a key-value in an object

```
// Dot notation
const obj = {};
obj.a = 1234;
/*
the object now looks like
{
  a: 1234
}
*/

// Bracket notation
const obj = {};
obj['a'] = 5123;
/*
the object now looks like
{
  a: 5123
}
*/
```

## Strings

Strings can be defined in three ways.

```
// double quotes
"this is an example"
// single quotes
'this is an example'
// string interpolation example
let x = 12341234;
`this is an example of string interpolation ${x}`
// the resulting interpolated string looks like
"this is an example of string interpolation 12341234"
```

## Values

The valid type of js values are

- numbers
- strings
- functions
- objects
- arrays
- undefined
- null
- Infinity
- -Infinity
