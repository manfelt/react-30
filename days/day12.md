# Day 12

**Date**: 20th Sept, 2020
**Time spent**: 3 hours

## Summary of yesterday

- Higher order components
- Render props
- Context

## Learnings

### 1. HTTP and React:

- To fetch data in React, there are many HTTP libraries available like - Apollo, Axios, Relay Modern, Request, and Superagent. I went with the Axios library. 

- I created a new React app: **npx create-react-app http-react**

- Installed Axios: **npm install axios**. After that, the package.json file should have updated all the dependencies. 



### 2. HTTP GET

- In the below example, **componentDidMount()** will be called once the component is mounted, so it will display a list of users from provided API. If the API is incorrect or does not return output, then the error message will be displayed.

```js
        componentDidMount(){  
            axios.get('https://reqres.in/api/users/')  
            .then(response => {  
                console.log(response.data.data)  
                this.setState({  
                    users:response.data.data  
                })  
            })  
            .catch(error =>{  
                this.setState({  
                    errorMessage:"Error fetching data"  
                })  
            })  
        }  

```

## Challenges

- Nothing
  
## Tomorrow's focus

- Laying the foundations for a new app
