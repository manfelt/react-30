# Day 09

**Date**: 17th Sept, 2020
**Time spent**: 3 hours

## Summary of yesterday

- Components life cycle
- Updating
- Unmounting

## Learnings

### 1. Pure components:

  - In React, a component is stated as pure only when it renders the same output for the same state and props and its return value is always the same for the same input values. 
  
  - Pure Component includes some performance improvements and renders optimization as React implements the shouldComponentUpdate() method for shallow comparison for props and state.
  
  - The term **Shallow comparison** is important when using Pure Component. Shallow Comparison refers to 2 primitive types, Primitive Type and Complex type,

In **Primitive Type**, for example we have 2 values, a and b of any type, like strings, boolean or numbers. A shallow comparison b returns true if both are of the same type and have the same value
```js
    let a = “Test”;  
    let b = “Test”;  
    console.log(a===b); // return true;  
```

In **Complex type** like arrays & object, a shallow comparison b returns true if both have the same objects.
```js
   let a = {1,2,3}  
   let b = {1,2,3}  
   let c = a  
   console.log(a===b); // return false; point to different object  
   console.log(a===c); // return true, as it points to the same object 
```

### 2. Fragments:

- In React, when returning any element in render() method, multiple elements must be wrapped within the main container. 

- To provide relief from adding a container to add multiple elements, the concept of Fragment was introduced. 

- Noted benefits:
  - Some css mechanisms like CSS Grid, Flexbox have some special parent-child relationship and adding div in the middle make it difficult to keep the desired layout while extracting logical components.
  - This provided a faster and use less memory as it does not create any additional node. This gives a benefit when the application is very large and using these fragments prevents creating unnecessary elements.
  - It provides increased render performance and less memory overhead.

**Return group of elements** is used below:
```js

    import React,{Component,Fragment} from 'react';  
      
    class Fragments extends Component{  
            constructor(props){  
            super(props);  
                    this.state={  
                            UserName : ''  
                    }  
            }  
      
            render(){  
                    return(  
                            <Fragment>  
                                    <label>Name : </label>   
                                    <input type='text' name='txtuser' id='textuser' value={this.UserName}/>  
                                    <button> Click Me !</button>  
                            </Fragment>  
                    )  
            }  
    }  
      
    export default Fragments;  

```

## Challenges

- Nothing
  
## Tomorrow's focus

- Memo
- Ref
