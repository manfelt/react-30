# Day 11

**Date**: 19th Sept, 2020
**Time spent**: 4 hours

## Summary of yesterday

- Memo
- Ref
- Portals

## Learnings

### 1. Higher order components(HOC):

  - It's a concept that involves the compositional nature of React.
  
  - A component transforms props into UI while on the other hand, a Higher-Order Component converts a component into another component.
  
  - The concept of Higher-Order Components is mainly used for reusability and for the decomposition of components into simple and smaller functions that can be reused. 

**Props proxy** as the name suggests, passes properties received from Higher-Order Component:
```js

    function ppHOC(WrappedComponent) {  
       returnclass PP extends React.Component {  
          render() {  
             return <WrappedComponent {...this.props}/>  
          }  
       }  
    }  
```

**Inheritance Inversion** allows HOC to access WrappedComponents instance using this keyword. This lets us access props, state, and render methods:
```js

    function iiHOC(WrappedComponent) {  
       return class Enhancer extends WrappedComponent {  
          render() {  
             return super.render()  
             }  
          }  
    }  

```

- Use cases for Higher Order Components:
  - 1. Loader to create a Higher-Order Component that can be used whenever required.
  - 2. Whenever needed to manage common user interaction.
  - 3. When a user needs to define some specific styles.
  - 4. You can create your dialogue as a component and can be used in the entire application.

### 2. Render props

- Render Props in React is something where a component’s prop is assigned a function and that is called in the render method of the component. 

- Calling the function will return a React element or component. 

- A render prop is a function prop that the component uses to know what to render. Through this, we can also pass a state to another.

### 3. Context

- Context in React.js is the concept to pass data through a component tree without passing props down manually to each level.

- Context lets you provide the functionality to share values among components without explicitly passing props through every level of the component tree.


## Challenges

- Nothing
  
## Tomorrow's focus

- HTTP & React
