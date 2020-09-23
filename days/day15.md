# Day 15

**Date**: 23rd Sept, 2020
**Time spent**: 2 hours

## Summary of yesterday

- Not actually organizing the code

## Learnings

### 1. Organizing the code

- React has a huge advantage: It doesn’t have any strict rules you have to follow. (However, doing it wrong, this also can be a huge downside, of course.)

-  Having certain patterns throughout the building procedure really helps you in keeping the app manageable.


### 1.1. Folder structure

- We distinguish between three different types of components in our application which can be ordered hierarchically, again:
  - **Elements** - Buttons, Icons, Inputs, etc. — all those are elements which are used over and over again. They are **low-level items**, reused in multiple components.
  - **Components** in the folder structure. A component has to fulfill a certain standalone function for the user or the app’s appearance. And so, it's not just an element. Elements, in contrast, doesn’t provide standalone functions. So whilst a search bar component allows the user to submit a search query, an input field alone won’t.
  - **Containers**. As a third and last type of component, there are containers. Containers are our state-managing components. They are at the very top of our hierarchy and usually consist of several components.
  - There are tons of approaches, all coming with different pros and cons. There might be other schemas to follow depending on the project. 

### 1.2 Class based vs functional components

- In React, we can write our components as class-based ones or functional ones. To always know which type you should use, here is a rule of thumb:
  - **If your class-based component only has a render method, make it a functional component.**

- Using functional components has a lot of benefits: They make your code cleaner and easier readable, they are better debuggable, and they are easier testable.
  - Thus, using them as often as you can, won’t hurt your application. 


## Challenges

- Short on time 😔
  
## Tomorrow's focus

- Building an app
