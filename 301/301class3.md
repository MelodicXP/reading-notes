# 301 - Class 3 - Passing Functions as Props

## Why this topic matters  

  This topic matters as it allows for a more dynamic approach in updating arrays and updating states between parent and children components.

## React Docs - lists and keys

1. **What does .map() return?**

    .map() returns a new array.

2. **If I want to loop through an array and display each value in JSX, how do I do that in React?**

    Use map() to iterate through array and set a unique 'key' prop for each item and store values as JSX elements using curly braces and return new array to be used as neeeded. (See Example Below (Example from ChatGPT))

    ``` javascript

    const items = [
    { id: 1, name: 'Item 1' },
    { id: 2, name: 'Item 2' },
    { id: 3, name: 'Item 3' },
    ];

    import React from 'react';

    class ItemList extends React.Component {
    render() {
      const items = [
        { id: 1, name: 'Item 1' },
        { id: 2, name: 'Item 2' },
        { id: 3, name: 'Item 3' },
      ];

      const itemElements = items.map((item) => (
        <li key={item.id}>{item.name}</li>
      ));

      return (
        <div>
          <h1>Item List</h1>
          <ul>{itemElements}</ul>
        </div>
      );
    }
    }

    export default ItemList;
    ```

3. **Each list item needs a unique ____.**  

    Key

4. **What is the purpose of a key?**  

    It helps React efficiently identify and update individual elements within the list when changes occur.  
  
    Key props help keep track of list items and efficiently update the DOM when changes occur. The key prop provides React with a way to differentiate between elements in the list. React uses these keys to determine which elements have been added, removed, or rearranged  

    Optimizes the rendering process. When an element changes or is removed, React can precisely update only the affected elements in the DOM, rather than re-rendering the entire list. This improves performance and reduces unnecessary work for the browser.

## The Spread Operator

1. **What is the spread operator?**

    The spread operator (...) in JavaScript is a an operator used to manipulate arrays, objects, and other iterable data structures. It allows you to "spread out" the elements of an iterable and use them in various ways such as combining arrays into one array.

2. **List 4 things that the spread operator can do.**  

    1. Replace apply() method - used when want to use elements of an array as arguments to a function.  

        ``` javascript

        function myFunction(x, y, z) {}
        const args = [0, 1, 2];
        myFunction.apply(null, args);
        ```  

        Can be re-writeen as:

        ``` javascript

        function myFunction(x, y, z) {}
        const args = [0, 1, 2];
        myFunction(...args);
        ```  

    2. Copying an array

        ``` javascript
        const arr = [1, 2, 3];
        const arr2 = [...arr]; // like arr.slice()

        arr2.push(4);
        // arr2 becomes [1, 2, 3, 4]
        // arr remains unaffected
        ```

    3. Concatenate arrays

        ``` javascript
        let arr1 = [0, 1, 2];
        const arr2 = [3, 4, 5];

        arr1 = [...arr1, ...arr2];
        // arr1 is now [0, 1, 2, 3, 4, 5]
        ```

    4. Copying and merging objects

        ``` javascript
        const obj1 = { foo: "bar", x: 42 };
        const obj2 = { bar: "baz", y: 13 };

        const mergedObj = { ...obj1, ...obj2 };
        // { foo: "bar", x: 42, bar: "baz", y: 13 }
        ```
  
3. **Give an example of using the spread operator to combine two arrays.**  

      ``` javascript
      let arr1 = [1, 2, 3];
      let arr2 = [4, 5, 6];

      // Use spread operator to combine arrays
      let combinedArr = [...arr1, ...arr2];

      console.log(combinedArr);

      // Output '[1, 2, 3, 4, 5, 6]'
      ```

4. **Give an example of using the spread operator to add a new item to an array.**  

    ``` javascript
    let array = [1, 2, 3];
    let newItem = 4;

    // Use spread operator to add new item  newArray
    const newArray = [...originalArray, newItem];

    console.log(newArray);

    // Output '[1, 2, 3, 4]'
    ```

5. **Give an example of using the spread operator to combine two objects into one**  

    ``` javascript
    let obj1 = { name: 'John', age: 30 };
    let obj2 = { city: 'New York', country: 'USA' };

    // Use spread operator to combine objects
    let combinedObj = { ...obj1, ...obj2 };

    console.log(combinedObj);

    // Output '{ name: 'John', age: 30, city: 'New York', country: 'USA' }'
    ```

## How to Pass Functions Between Components

1. **In the video, what is the first step that the developer does to pass functions between components?**

    Create the function wherever the state is that is going to be changed.

2. **In your own words, what does the increment function do?**  

    Summary: Check to see if a given name matches a name from people array and if so update the count of the matching name, and update people array with updated count. Steps below:  

    Take in a name as an argument and use map() method creates a new array (which holds updated data).  

    If any name in people array matches name argument, increase count of person object in people array that matches name argument and return updated person object.  

    Update state of people array with updated array.

3. **How can you pass a method from a parent component into a child component?**  

    Calling the child component upon which the method is passed as a prop to child.

4. **How does the child component invoke a method that was passed to it from a parent component?**

    Via the prop.  
    _'this.props.nameOfMethod(argument)'_

## Links to resources used for these notes

* [Lists and Keys](https://legacy.reactjs.org/docs/lists-and-keys.html)
* [The Spread Operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)
* [How to Pass Functions Between Components](https://www.youtube.com/watch?v=c05OL7XbwXU)
* ChatGPT
