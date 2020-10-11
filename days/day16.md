# Day 15

**Date**: 23rd Sept, 2020
**Time spent**: 2 hours

## Summary of yesterday

- 

## Learnings

### 1. Gathering data from API

- In this day I've been poking at how to fetch data from an API

- I've been working on a script which should work on a json array, fetching data from https://jsonplaceholder.typicode.com/users, which works fine, however, trying the same script at https://api.met.no/weatherapi to get some weather results proved problematic. More on this coming up next. For the moment, the script is as below.


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

    fetch('https://api.met.no/weatherapi/locationforecast/2.0/compact.json?lat=59.9&lon=10.75')
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
              <li key={item.index}>
                Name: {item.type} | Email: {item.geometry}
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
