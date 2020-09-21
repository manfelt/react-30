# Day 13

**Date**: 21th Sept, 2020
**Time spent**: 3 hours

## Summary of yesterday

- HTTP and React
- HTTP GET

## Learnings

### 1. Laying the foundations for a new app

- This will be the overall theme for this day. 

- As I will dive into the preparations, I'm going to break down the steps taken towards realizing a project in React. 

### 1.1 Mockup

- As good practice, when planning the app, it's good to create a visual image of how the results will look

- This will either be strictly how it is going to become, or at least an idea of it.

- Splitting the UI into independent elements and thus React components. 

- One can use whatever method one likes, be it through software designed for creating mockups, or more crudely; in windows paint or by pen and paper.

### 1.2 Break the UI into components

- After mockup, one can begin identifying the app's components.

- If one is unsure whether an element should fit in it's own component, & which don't there's always the **single responsibility principle**: https://en.wikipedia.org/wiki/Single-responsibility_principle


### 1.3 Arrange all components hierarchically

- After having identified all components, arranging them in a hierarchy is the next step in our planning process.

- It will makes the componetn's dependencies clear and will help when implementing data flows in the app.


You can create such a hierarchy by having a look at the mockup and see which components are nested inside each other. For instance, the search bar component contains the input field and button as child components. So these two children are hierarchy-seen below the search bar component.
```
App
|__Header
| |__Logo
|__Search bar
| |__Input field
| |__Button
|__Card
| |__Weather details
|   |__Icon
|   |__Temperature
|   |__Description
|   |__Date
|__Footer
| |__Logo
```

### 1.4 Define where state should live

- As a last step in the planning process, we need to define components which should manage the application’s state.

- As recommended in the React docs, we want to have a top-down data flow. This means that ideally there is one single source of truth at the top of our main application and from this source, all information flows downwards like a waterfall.

- In general, it is recommended to have as few stateful components as possible.


## Challenges

- Nothing
  
## Tomorrow's focus

- Organizing the code
