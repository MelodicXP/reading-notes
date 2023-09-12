# 301 - Class 2 - States and Props

## Why this topic matters  

  This topic matters is it covers the differences and applications as it relates to React props vs React state.

## React lifecycle

1. **Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?**

    'Render' occurs first.

2. **What is the very first thing to happen in the lifecycle of React?**

    Mounting occurs first.  Mounting is kicked off by calling constructor for a React componenet before it is mounted (if the component is a sub-class, should call super(props)).  Then can proceed with Mounting.

3. **Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates**  

    1. constructor
    2. render
    3. componentDidMount
    4. React Updates
    5. componentWillUnmount

4. **What does componentDidMount do?**  
  Its purpose is to perform actions that need to happen after the component is displayed, such as data fetching from an API (Youtube), setting up subscriptions, network requests, or interacting with the DOM, ensuring that these actions occur only once after the initial rendering.

## React State Vs Props

1. **What types of things can you pass in the props?**

    Various types of data can be passed in props such as strings, numbers, booleans, objects, functions, React Elements, and arrays.

2. **What is the big difference between props and state?**

    Props and its data are handled outside the component.  State is data that is managed and updated within the component.

3. **When do we re-render our application?**  

    Every time state is updated it typically triggers a re-render of the component and any children of that component.

## Links to resources used for these notes

* [React Lifecycle](https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093)
* [React State vs Props](https://www.youtube.com/watch?v=IYvD9oBCuJI)
