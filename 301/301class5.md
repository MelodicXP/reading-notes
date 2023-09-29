# 301 - Class 5 - Putting it all together

## Why this topic matters  

  This topic matters is it covers

## React Docs - Thinking in React

1. **What is the single responsibility principle and how does it apply to components?**

    A component should ideally only do one thing.  If complexity of component grows, it should be decomposed into smaller subcomponents.  

2. **What does it mean to build a ‘static’ version of your application?**

    Build a version that renders UI from data model without any interactivity.  

3. **Once you have a static application, what do you need to add?**  

    Make the UI interative using 'state'. Allows user to change underlying data model.

4. **What are the three questions you can ask to determine if something is state?**

    * Does it remain unchanged over time? If so, it isn’t state.
    * Is it passed in from a parent via props? If so, it isn’t state.
    * Can you compute it based on existing state or props in your component? If so, it definitely isn’t state!

5. **How can you identify where state needs to live?**

    1. Identify every component that renders something based on that state.
    2. Find their closest common parent component—a component above them all in the hierarchy.
    3. Decide where the state should live:
        1. Often, you can put the state directly into their common parent.
        2. You can also put the state into some component above their common parent.
        3. If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common parent component.

## Higher-Order Functions

1. **What is a “higher-order function”?**

    Functions that operate on other functions, either by taking them as arguments or by returning them.

2. **Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?**

    It returns another function that can be used later on depending on the argument passed into it.

3. **Explain how either map or reduce operates, with regards to higher-order functions.**

    Both map and reduce take functions as arguments which means both are considered higher-order functions.  

    _map()_ - takes a function as an argument and returns a new array. Takes an existing array, processes each element of that array with a provided function, and returns a new array with the results.  

    _reduce()_ - takes a function as an argument and returns a single value. It "reduces" an array into a single value by applying a provided function to each element and accumulating the results.

## Links to resources used for these notes

* [Thinking in React](https://react.dev/learn/thinking-in-react)
* [Higher-Order Functions](https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK)
