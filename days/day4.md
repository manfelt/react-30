# Day 04

**Date**: 12th Sept, 2020
**Time spent**: 3 hours

## Summary of yesterday

- JSX
- Hooks
- Props

## Learnings

### 1. State:

  - A State in React can be changed as per the user action or any other actions. When the state is changed, React then re-renders the component automatically to the browser.
  
  - React stores the state of a component in this.state. 
  
  - When a state is changed, it then follows that the component becomes re-rendered. Anyways, here's how you use states in React:
  
  ```js
import React from 'react';

// create state variable
// syntax: const [stateVariable] = React.useState(defaultValue);
function App() {
  const [language] = React.useState('javascript');
  // we use array destructuring to declare state variable

  return <div>I am learning {language}</div>;
}
  ```


### 2. Destructuring props and states:

- It is a JavaScript feature that allows the users to extract multiple pieces of data from an array or object and assign them to their own variable. 


```js
    const book = {  
        title : "The Call of Cthulhu",  
        author:"H.P.Lovecraft",  
        pages:"43"  
    }

```
Before ES6, you need to access properties as below.

```js
    console.log(book.title);  
    console.log(book.author);  
    console.log(book.pages); 
```

Destructuring let us distribute this code.

```js
    const {title,author,pages} = book 
```

Which is the same as this:

```js
    const title = book.title;  
    const author = book.author;  
    const pages = book.pages;  
```

The properties above can thus be accessed without the 'book'-prefix: 

```js
    console.log(title);  
    console.log(author);  
    console.log(pages);  
```
### 3. Basic event handling:

- A handler determines what actions need to be taken when an event is fired. 

- In React, all event handlers are defined in camel case, i.e., in JavaScript onclick will be defined as onClick() in React application.

- Unlike in HTML, in JSX, we pass a function as an event handler rather than a string.

```js
    // Note: most event handler functions start with 'handle'
    function handleToggleTheme() {
    // code to toggle app theme
    }

    // in html, onclick is all lowercase
    <button onclick="handleToggleTheme()">
     Submit
    </button>

    // in JSX, onClick is camelcase, like attributes / props
    // we also pass a reference to the function with curly braces
    <button onClick={handleToggleTheme}>
     Submit
    </button>
```


## Challenges

- Nothing
  
## Tomorrow's focus

- Conditional rendering
- List rendering
- Binding method and event handler as props
