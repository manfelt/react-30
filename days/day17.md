# Day 17

**Date**: 13th Oct, 2020
**Time spent**: 1 hour

## Summary of yesterday

- 

## Learnings

### 1. Gathering data from API again

- The snippet from the previous day should produce output which is supposed to be gathered from **https://jsonplaceholder.typicode.com/users**

- This should give an array of names attached to email adresses.


```js
import React, { Component } from 'react';

class App extends Component {

  constructor(props) {
    super(props);
    this.state = {
      items: [],
      isLoaded: false,
    }
  }

  componentDidMount() {

    fetch('https://jsonplaceholder.typicode.com/users')
    .then(res => res.json())
    .then(json => {
      
      this.setState({
        isLoaded: true,
        items: json.items,
      })
    });
  }

  render() {

    var { isLoaded, items } = this.state;

    if(!isLoaded) {
      return <div>Loading...</div>;
    }

    else {}

    return (
      <div className="App">
        Data has been loaded 

        
        <ul>
          {items.map(item => (
              <li key={item.id}>
                Name: {item.name} | Email: {item.email}
              </li>
          ))}
        </ul>
    </div>
    );
  }
}

export default App;


```


## Challenges

- Short on time 😔
  
## Tomorrow's focus

- Working on the script
