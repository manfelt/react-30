# Day 07

**Date**: 15th Sept, 2020
**Time spent**: 2,5 hours

## Summary of yesterday

- Conditional rendering
- List rendering

## Learnings

### 1. Forms In React:

  - Form in React works the same way as it works in HTML.
  
  - They provide us a basic medium to the user to interact with the app.
  
  - For the sake of functionality, there are techniques called **Controlled Components** and **Uncontrolled Components**. Both of those are on today's topics. 


### 2. Uncontrolled Components:

- The Uncontrolled components are those components that store and maintain their own state internally. 

- This component is just like traditional HTML forms because the input form data is stored inside DOM and not within the component. Elements like <input> and <textarea> maintain their state by themselves. 

- We can get input values from DOM using `ref`.
  

Here, the <input> component stores its state. The ref attribute is used to create a reference to the DOM and made it accessible from where you can pull the values when needed.
```js
import React,{Component} from 'react';
// import styled from 'styled-components';

class UserForm extends Component {
    constructor(props) {
        super(props);
        this.handleSubmit = this.handleSubmit.bind(this);
    }

    handleSubmit(e) {
        alert('Input value is :'+ this.input.value);
    }

    render(){
        return(
            <form onSubmit={this.handleSubmit}>
                <label>Enter Name</label>
                <textarea type="text" ref={(input) => this.input = input}></textarea>
                <button type="submit">Submit</button>
            </form>
        )
    }
}

export default UserForm;
```

### 3. Controlled Components:

- The Controlled component in React is used to control the values of input form elements.

- A Controlled Components has two aspects
  - Controlled components have functions to handle the data going into them on every OnChange event, rather than grabbing data at once. For example, whenever user clicks submit button. This passed data is then saved to the state
  - Data displayed by a controlled component is received through props passed down from its parent/container component.
  
- React follows unidirectional flow which means there is a one-way loop, from child component input to parent component state and back down to child component via props.

- **Container component** is the one which process data, has business logic or make data calls so they are also known as Smart components while on the other hand Dumb component just receive data from the parent container. 

- List of **dumb components**:
  - button
  - textarea
  - input
  - select
  - checkbox
  
```js
          render(){  
                return(  
                        <form onSubmit={this.handleSubmit}>  
                                <Input name={"inputText"} title={"FullName"}      value={this.state.UserName}  
                                placeholder={"Enter Name"}   
                                handleChange={this.state.handleChange}></Input>  
                                <button type="submit">Submit</button>  
                        </form>  
   
```

## Challenges

- Finally caught up with my work. I had to make up for two days this day because I was lagging behind a day. But, i've now covered an entire week! 🥳
  
## Tomorrow's focus
- Components Life Cycle
- Updating
- Unmounting
