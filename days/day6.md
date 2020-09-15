# Day 06

**Date**: 14th Sept, 2020
**Time spent**: 3 hours

## Summary of yesterday

- Method as props
- Binding method and event handler as props

## Learnings

### 1. Conditional reandering:

  - Conditional rendering is f.ex **control structure**, which is to say it directs the order of execution of the statements in a program.
  
  - 5 methods to design conditional rendering:
    - If/else
    - Element variables
    - Ternary operator
    - Short-circuit operator
    - IIFE (Immediately Invoked Function Expression)
  
  
Here is an example of if/else:  
  ```js
const greeting = <div>Hello React</div>;

const isNewToReact = true;

// Expressions can be displayed conditionally
function sayGreeting() {
  if (isNewToReact) {
    // ... or returned from functions, etc.
    return greeting; // displays: Hello React
  } else {
    return <div>Hi again, React</div>;
  }
}
```

### 2. List rendering:

- In React, List array can have many ways to display in the browser.

- Using array index
  - List items can be displayed in the browser using the array index.
  - A convenient solution, but it becomes inefficient as the number of array is large.
  
```js
import React from 'react';

function BookList() {
    const book = ['zbc','xyz'];
    return(
        <div>
            <h2>{book[0]}</h2>
            <h2>{book[1]}</h2>
        </div>
    )
}

export default BookList;
```

- **Array.map()**. This method makes it easier to render arrays, makes for better readability and is more efficient compared to using array indexing.

```js
// This will output the exact same as the snippet of code above.
import React from 'react';
      
function BookList(){    
      const book = ['abc','xyz'];    
         
      return(    
          <div> {book.map(bok => <h2>{bok}</h2>)} </div>    
       )    
}  

export default BookList; 
```

Which also works excellent when faced with somethin more complex. Like this array with key-value pair in each array, having multiple values:
```js
import React from 'react';
      
function BookList(){
    const book = [{
        title:'The Trial',
        author:'Kafka',
        genre:'Dystopian Fiction'
    },{
        title:'Hunger',
        author:'Hamsun',
        genre:'Psychological novel'
    },{
        title:'The Stranger',
        author:'Camus',
        genre:'Psychological novel'
    }
    ];

    const bookList = book.map(bok => <h2>The title of this book is {bok.title}. It is a {bok.genre} written by {bok.author} </h2>);

    return(
        <div>
            {bookList}
        </div>
    )
}
export default BookList; 
```


## Challenges

- Nothing
  
## Tomorrow's focus
- Forms In React
- Uncontrolled Components
- Controlled Input
