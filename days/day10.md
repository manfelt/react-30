# Day 10

**Date**: 18th Sept, 2020
**Time spent**: 4 hours

## Summary of yesterday

- Pure Components
- Fragments

## Learnings

### 1. Memo:

  - The concept named **Memo** is a function-based component, unlike **Pure Component** which is a class-based component.
  
  - **React.memo()** is a higher-order component same as React.PureComponent(). It also provides a performance boost.
  
  - If the function component renders the same result using the same props, it can be wrapped in React.memo() for performance enhancement. This means that React will skip rendering the component and reuse the last rendered result.
  
  - In the console, the memo component is rendered once and after that, it is not rendered until any changes occur in props or state.

### 2. Ref:

- Refs in React make it possible to access DOM nodes directly without using props or re-rendering a whole component.


Let’s look at an example to change the input element without using props:
```js

    import React, { Component } from 'react'  
      
    class RefsDemo extends Component {  
            constructor(props) {  
                    super(props);   
                    this.inputRef = React.createRef()  
            }  
      
            componentDidMount(){  
                    this.inputRef.current.focus();  
                    console.log(this.inputRef)  
            }  
      
            clickHandler = () => {  
                    alert(this.inputRef.current.value)  
            }  
      
            render() {  
                    return (  
                            <div>  
                                    <input type="text" ref={this.inputRef}/>  
                                    <button onClick={this.clickHandler}>Click Me!</button>  
                            </div>  
                    )  
            }  
    }  
      
    export default RefsDemo  


```

### 3. Portal:

- A React Portal is a way of binding an element outside of its component hierarchy, in a separate component.

- Portals are mostly used for implementing, Tooltip, Modals, Global message notifications, hovercards, chat widgets, and Floating menus.

- We can return strings, numbers, components, React portals or an array of children.

## Challenges

- Nothing
  
## Tomorrow's focus

- Higher order components
