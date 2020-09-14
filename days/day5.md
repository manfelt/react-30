# Day 04

**Date**: 13th Sept, 2020
**Time spent**: 3 hours

## Summary of yesterday

- State
- Destructuring props and states
- Basic event handling

## Learnings

I have deviated some for this day's plan. 

### 1. Method as props:

  - Used to share code between React components using a prop whose value is a function.
  
  - It is used to share the state of one component to another component that needed the same state.
  
  
  ```js
import React, { Component } from 'react'; 
import ChildComponent from './ChildComponent'; 
  
class ParentComponent extends Component { 
    constructor(props) { 
        super(props); 
       
        this.state = { 
            parentName:'Parent'
        } 
   
        this.greetParent = this.greetParent.bind(this) 
    } 
       
    greetParent() { 
        alert(`Hello ${this.state.parentName}`) 
    } 
   
    render() { 
        return ( 
            <div> 
                <ChildComponent greetHandler={this.greetParent}/> 
            </div> 
        ) 
    } 
} 
  
export default ParentComponent;
```

### 2. Binding method and event handler as props:

- In React, there are 4 ways to bind event handlers.

  - One can use **bind()** within the **render()** function.
  - Or use an arrow function body in the render method.
  - Bind in the constructor.
  - And using the class property as an arrow function. 

```js
import React from 'react';  
  
class EventBinding extends Component{  
         constructor(props){  
               super(props)  
               this.state = {  
                     message : "Testing"  
               }  
         }  
  
        clickHandler(){  
               this.setState({  
                         message : "Tested"  
               })  
         }  
  
        render(){  
               return(  
                  <div> {this.state.message}  
                           <button onClick={this.clickHandler.bind(this)}>Test</button>  
                  </div>  
        );  
    }  
}  
  
export default EventBinding;  
```


## Challenges

- Nothing
  
## Tomorrow's focus
- Conditional rendering
- List rendering
