# Day 01

**Date**: 9th Sept, 2020
**Time spent**: 4

## Summary of yesterday

Nothing

## Learnings

- There are prerequisites to learning react

  - **Javascript Es6**:  It is a JavaScript standard meant to ensure the interoperability of Web pages across different Web browsers.

### 1. HOC or 'Higher Order Component':

- A Higher Order Component is an advanced technique in React for reusing component logic in applications. 

- It takes a component and returns a new Component. 

### 2. Styling React:

- React Native gives us a css-like way to style our components. If you've used css modules, things should look very familiar. Except with differences

- In React, inline styles are not specified as a string. Instead they are specified with an object whose key is the camelCased version of the style name, and whose value is the style’s value, usually a string.


  ```js
 import React from 'react';

const divStyle = {
  margin: '40px',
  border: '5px solid pink'
};
const pStyle = {
  fontSize: '15px',
  textAlign: 'center'
};

const Box = () => (
  <div style={divStyle}>
    <p style={pStyle}>Get started with inline style</p>
  </div>
);

export default Box;
  ```



## Challenges

  - For the moment, a challenge is to collect an overview and understanding of what lies ahead of me. Which knowledge do I need to hold to move forward, and am I even on secure footing with what I already know?
  
  
## Tomorrow's focus

- Flexbox for react native
- Custom fonts
- React navigation
