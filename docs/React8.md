---
id: React8
title: Hooks
sidebar_label: Hooks
---

Hooks are functions that let you “hook into” React state and lifecycle features from function components. Hooks don't work inside classes, They let you use React without classes.You can also create your own Hooks to reuse stateful behavior between different components.

[Hooks API Reference - React Docs](https://reactjs.org/docs/hooks-reference.html)

### State Hook

The State Hook, `useState` is a Hook , We call it inside a function component to add some local state to it. React will preserve this state between re-renders. useState returns a pair: the current state value and a function that lets you update it.

```js
import React, {useState} from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  );
}
```

### Effect Hook

The Effect Hook, `useEffect` adds the ability to perform side effects from a function component. It serves the same purpose as componentDidMount, componentDidUpdate, and componentWillUnmount in React classes, but unified into a single API.

```js
import React, {useState, useEffect} from 'react';

function Example() {
  const [count, setCount] = useState(0);

  // Similar to componentDidMount and componentDidUpdate:
  useEffect(() => {
    // Update the document title using the browser API
    document.title = `You clicked ${count} times`;
  });

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>Click me</button>
    </div>
  );
}
```

## Rules of Hooks

Hooks are JavaScript functions, but you need to follow two rules when using them. We provide a linter plugin to enforce these rules automatically:

**Only Call Hooks at the Top Level**

Don’t call Hooks inside loops, conditions, or nested functions. Instead, always use Hooks at the top level of your React function, before any early returns. By following this rule, you ensure that Hooks are called in the same order each time a component renders. That’s what allows React to correctly preserve the state of Hooks between multiple useState and useEffect calls.

**Only Call Hooks from React Functions**

Don’t call Hooks from regular JavaScript functions. Instead, you can:

1. Call Hooks from React function components.
2. Call Hooks from custom Hooks (we’ll learn about them on the next page).
