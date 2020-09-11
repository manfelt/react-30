# Day 02

**Date**: 10th Sept, 2020
**Time spent**: 3



## Summary of yesterday

- Started on a react tutorial
- Set up environment for development
- Some fundamentals of starting a react app
- Explored concepts from ES6, arrow functions etc

## Learnings

### 1. Folder structure:

In order to start a react app, one may choose to utilize `create-react-app node_module`. 
From the terminal, running `npx create-react-app` will create a new folder containing files for a react app to run, which saves time for the developer.

### 2. Components

Components are snippets of code within the file which can be run multiple times.

There are two types of components: 
- Stateless functional component
- Stateful class component

Stateless functional component includes simple JavaScript functions. These components include immutable properties, i.e., the value for properties cannot be changed. A functional component is used mainly for UI.
``` 
    function Demo(props) {  
       return <h1> Hello, {props.Name} </h1>;  
    }  
```

The Class component is ES6 classes which extend the Component class from React library. The class component must include the render method which returns HTML.
```
    class Demo extends React.Component{  
       render(){  
       return <h1> Hello, {props.Name} </h1>;  
       }  
    }  
```

## Challenges
N/A

## Tomorrows focus
- Reactjs JSX
- Props
- Hooks
-
