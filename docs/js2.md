---
id: js2
title: Basic Syntax
sidebar_label: Basic Syntax
---

- Dive into core syntax
- Understand variables & data types
- Work with operators
- Explore & user function
- Scope & type conversion

### Adding Javascript

**Internal** - `<script>alert("Hello World") </script>`<br/> **External** - `<script src="assets/scripts/app.js"></script>`

### Variables & Constants

Variables is a data container - let userName = 'Max';<br/> Where the value can change - userName = 'Maxi';

Constant is also a data container - `const total = 15;`<br/> Where value must not change - `totalUser = 20;`

**Naming Convention**

let userName [ camelCase ]<br/> let ageGroup5 [ only letter & digits ] <br/> let $kindOfSpecial [ Starting with $ ]<br/> let \_internalValue [ Starting with \_ ]<br/>

Constant - const ATTACK_VALUE = 10;<br/> Event Listener - onClick or clickHandler

**Bad Practice**

- `let user_name` [ Bad ]
- `let 21Players` [ Starting with digit]
- `let user-b` [ No special characters ]
- `let let` [ keywords not allowed ]

### Operators

Add two number [ + ]<br/> Subtract two number [ - ]<br/> Multiply two number [ * ]<br/> Divide two number [ / ]<br/> Divide two numbers,remainders [ % ]<br/> Exponentiation [ ** ] [2**3 = 8]<br/> Assign value to variable [ = ]<br/> Perform calculation and reassign result to variable [ +=, -= ]<br/> Increment / Decrement<br/> variable value + re-assign [ ++,-- ]<br/>

### Data types

**Primitives**

- Numbers - 2,-3,22.66
- Strings - 'Hi', "Hello", `Hello`
- Booleans - true / false
- Null & Undefine

**Reference**

- Objects - { name: 'Max', age: 31 }
- Arrays - [1, 3, 5] ( Special Object )
- Function - function(){}

:::note Data Copy<br/><br/> Primitives are copied by value<br/> References are copied by reference

:::

String Interpolation `(${defaultResult}+10)*3/2-1)`

### Functions

A function is a procedure—a set of statements that performs a task or calculates a value,

```js title="Function"
function greetUser(name) {
  alert(`hi ${name}`);
}

greetUser('Max');
```

### Global & Local Scope

```js title="Global Scope"
let result; // GLOBAL
function add(num1, num2) {
  result = num1 + num2; //Success
}
```

```js title="Local Scope"
function add(num1, num2) {
  let result; //LOCAL
  result = num1 + num2;
}

console.log(result); //Error
```

```js title="Shadowed variables"
let userName = 'Max';
function greetUser(name) {
  let userName = name;
  alert(userName);
}
userName = 'Manu';
greetUser('Max');

//This will actually show an alert
//that says 'Max' (NOT 'Manu').
```

You might've expected that an error gets thrown because we use and declare userName more than once - and as you learned, that is not allowed.

It indeed is not allowed on the same level/ in the same scope.

### Type Conversion

**FYI - Every HTML input will always be string**

- parseInt() - convert string into number
- parseFloat() - convert string into float
- toString() - convert to String

**SHORTCUT**

- Conversion to number (currentResult = currentResult + +value)
- (A=A+B) = (A+=B)
- (A=A+1) = (A++)
- (++A) = Increment before assigning
- (A++) = Increment after assignig

### Array

JavaScript arrays are used to store multiple values in a single variable.

```js title="Array"
let fruits = ['Banana', 'Orange', 'Apple', 'Mango'];
fruits.pop(); // Removes the last element
fruits.push('Kiwi'); //  Adds a new element ("Kiwi") to fruits
```

### Objects

```js title="Objects"
var car = {
  type: 'Fiat',
  model: '500',
  color: 'white',
};

//ACCESSING OBJECT PROPERTIES
objectName.propertyName;
objectName['propertyName'];
```

### Null & Undefined

**Undefined**

1. Default value of uninitialized variables

2. You shouldn’t assign undefined as a value manually

**Null**

1. Never assumed by default
2. You can assign this is a value if you want to “reset” / “clear” a variable

**NaN**

1. Technically, it’s of type number and can therefore be used in calculations

2. It yields a new NaN and it’s the result of invalid calculations

### Types

- typeof 'Max' = String
- typeof 2 = Number
- typeof [1,2,3] = Object
- typeof {name:'Amarjit'} = Object
- typeof undefined = undefined
- typeof null = object
- typeof NaN = Number

## Useful Links

1. [JavaScript Basics](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
2. [Variables](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Variables)
3. [Operators](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Math)
4. [Functions](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Functions)
5. [Arrays](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Arrays)
6. [Objects](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics)
