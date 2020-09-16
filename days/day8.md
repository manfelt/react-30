# Day 08

**Date**: 15th Sept, 2020
**Time spent**: 1,5 hours

## Summary of yesterday

- Forms in React
- Uncontrolled components
- Controlled components

## Learnings

### 1. Components life cycle:

  - Every React component has it own lifecycle.
  
  - **Mounting** is the first stage, which is done within **constructor()**
    - First the constructor of component method is called before every other method is called. Why? To initialize props and state and to bind event handlers to the instance.
    - Then **static getDerivedStateFromProps()**, which is called just before **render()**. This method is used when the state of the component depends on props. 
    - **render()**. This method is the only required method in the class component. The render() function does not modify state component.
    - Lastly **componentDidMount()** It's called just after component is mounted (inserted into the tree). 


### 2. Updating:

- Used when some component needs to be re-rendered due to changes in either state or props.

- This phase has 5 different procedures: 
  - 1st: **static getDerivedStateFromProps()**. This method is called every time the component is re-rendered. it takes state and/or props as parameters. 
  - 2nd: **render()**. Which is the only required method in any React class component. This method reads state and props which in return provides JSX. 
This method does not change any value of props and state or make any interact with DOM or make any ajax calls.
  - 3rd: **getSnapshotBeforeUpdate()**. Called just **before** any changes are going to be updated in Real DOM from virtual DOM. If it is required to know the exact DOM available just before updating the result of latest render call.
  - 4th: **componentDidUpdate()**. This method is called **after** all the changes are updated in the DOM.
  - 5th: **shouldComponentUpdate()**. This method re-renders on every state change.This method defines if the component should be re-rendered or not. This method provides performance optimization.
  
Here is an example of the methods.
```js

    import React,{Component} from 'react';  
    import LifecycleChild from './LifecycleChild';  
              
    class Lifecycle extends Component{  
            constructor(props){  
                    super(props);  
                    this.state={  
                            value:'React Application'  
                    }  
                    this.changeState = this.changeState.bind(this);  
                    console.log("React Application constructor");  
            }  
      
            static getDerivedStateFromProps(props,state){  
                    console.log("React Application getDerivedStateFromProps");  
                    return null;  
            }  
      
            componentDidMount(){  
                    console.log("React Application componentDidMount");  
            }  
      
            shouldComponentUpdate(){  
                    console.log("React Application shouldComponentUpdate");  
                    return true;  
            }  
      
            getSnapshotBeforeUpdate(prevProps,prevState){  
                    console.log("React Application getSnapshotBeforeUpdate");  
                    return null;  
            }  
      
            componentDidUpdate(){  
                    console.log("React Application componentDidUpdate");  
            }  
      
            changeState = () => {   
                    this.setState({  
                            value : "React Application started"  
                    })  
            }  
      
            render(){  
                    console.log("React Application render");  
                    return(  
                            <div>  
                                    <div>Lifecycle Parent</div>  
                                    <button onClick={this.changeState}>Click Me</button>  
                                    <LifecycleChild></LifecycleChild>  
                            </div>  
                    );  
            }  
    }  
      
    export default Lifecycle;  
```

### 3. Unmounting:

- **componentWillUnmount()**
  - This method is used for canceling network requests or removing event handlers, invalidating timers or cleaning any subscriptions created using componentDidMount().

## Challenges

- Nothing (do I know this?)
  
## Tomorrow's focus
- Pure Components
- Fragments
- A surprise
