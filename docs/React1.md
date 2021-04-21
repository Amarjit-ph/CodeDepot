---
id: React1
title: React
sidebar_label: Introduction
---

[React Developer Roadmap](https://roadmap.sh/react) - Everything that is there to learn about React and the ecosystem in 2021.

React is a JavaScript library for building user interfaces. It is maintained by Facebook and a community of individual developers and companies. React can be used as a base in the development of single-page or mobile applications, as it is optimal for fetching rapidly changing data that needs to be recorded.

## Exploring JSX

It is a syntax extension to JavaScript. We recommend using it with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript. JSX produces React “elements”.

1. JSX stands for JavaScript XML.
2. JSX allows us to write HTML in React.
3. JSX makes it easier to write and add HTML in React.

```jsx title="JSX"
let template = (
  <div>
    <h1> Amarjit Pheiroijam</h1>
    <h2> Sagolband Thangjam Leirak </h2>
    <h3> Computer Science Engineer </h3>
  </div>
);
```

This funny tag syntax is neither a string nor HTML.

It is called JSX, and it is a syntax extension to JavaScript. We recommend using it with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript, JSX produces React “elements”.

## JSX Expressions

After compilation, JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects. This means that you can use JSX inside of if statements and for loops, assign it to variables, accept it as arguments, and return it from functions:

`{ }` - Use Bracket to write Javascript to render template<br/> `()` - JSX should be inside a bracket

```js title="JSX Expression"
let user = {
  name: 'Amarjit Pheiroijam',
  age: 23,
  Address: 'Chandigarh',
};

let template2 = (
  <div>
    <h1> NAME : {user.name} </h1>
    <h1> AGE : {user.age} </h1>
    <h1> LOCATION : {user.Address} </h1>
  </div>
);
```

## Conditional Rendering in JSX

In React, you can create distinct components that encapsulate behavior you need. Then, you can render only some of them, depending on the state of your application.

```js title="Conditional Rendering"
var user = {
  name: 'Amarjit Pheiroijam',
  age: 29,
  Address: 'Chandigarh',
};

// condition ? exprIfTrue : exprIfFalse

// STYLE 1
function getLoc(location) {
  if (location) {
    return <h1>LOCATION : {location}</h1>;
  } else {
    return undefined;
  }
}

// STYLE 2
var template3 = (
  <div>
    <h1> NAME : {user.name ? user.name : 'Anonymous'} </h1>
    <h1> AGE: {user.age && user.age >= 18 && user.age}</h1>
    {getLoc(user.Address)}
  </div>
);
```

[Manual Data Binding](https://gist.github.com/Amarjit-ph/9e36f62afaa6a9803a5c253a54a7058c)
