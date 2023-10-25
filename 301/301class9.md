# 301 - Class 9 - Functional Programming

## Why this topic matters  

  This topic matters as it will be incorporated in to functional programming.

## An Introduction to Node.js on sitepoint.com

1. **What is functional programming??**  

    Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.  
    Its like treating your program like a recipe book with step-by-step instructions, and once you've followed those instructions and produced a result, you don't go back and change things. This approach helps prevent unexpected side effects and makes it easier to understand and reason about your code.
  
2. **What is a pure function and how do we know if something is a pure function?**

    * It returns the same result if given the same arguments (it is also referred as deterministic)
    * It does not cause any observable side effects  
    It takes some inputs, performs a specific task, and always produces the same result with those inputs. It doesn't mess with anything else in the system; it just does its job. That's how we know if something is a pure function in programming.

3. **What are the benefits of a pure function?**

    * **Predictability:** Since pure functions always produce the same output for the same input, they are highly predictable. This predictability simplifies debugging and makes it easier to reason about your code.

    * **Testability:** Pure functions are easy to test. You can pass in different inputs and compare the output with expected results. This makes unit testing straightforward and reliable.

    * **Reusability:** Pure functions are modular and independent. You can use them in various parts of your codebase without worrying about unexpected side effects. This promotes code reuse and maintainability.

    * **Reasoning:** Pure functions make it easier to reason about your code's behavior. You don't need to consider hidden dependencies or global state changes when working with them.

    * **Optimizations:** Compilers and runtime environments can optimize pure functions more effectively because they don't need to account for unexpected side effects.

    Pure functions contribute to code that is easier to understand, test, and maintain. Allows to make more efficient software.

4. **What is immutability?**

     Immutability means that once you create a piece of data, like a number or a list, you can't change it directly. If you want to make a change, you create a new piece of data with the desired modifications

5. **What is Referential transparency?**

    Referential transparency means that if you use a function with the same inputs (or arguments), it will always produce the same output. Don't have to worry about unexpected surprises when calling a function because it behaves the same way every time it's used.

## Node JS Tutorial for Beginners #6 - Modules and require()

1. **What is a module?**  

    A module as a little package of code that encapsulates a specific functionality. It's like having a toolbox where each tool is neatly organized in its own compartment.  A Node.js module is a self-contained unit of code that you can use to add specific features or functionality to your applications without creating a tangled mess of code.

2. **What does the word ‘require’ do?**

    Lets system know that we want to use specific file from directory.

3. **How do we bring another module into the file the we are working in?**  

    use require('./name-of-file);

4. **What do we have to do to make a module available?**

    In the module use the line of code:  
    _'module.exports = counter;'_  
    at the end of the count.js file (for example), which makes _counter() function_ available from _count.js module_.  
    Next, in _app.js_ where _counter() function_ is to be used, use the line of code:  
    _var counter = require('/.count)_  
    which means _counter() function_ is being set to a variable called _counter_, which can then be used within _app.js_ to invoke and use _counter() function_.

## Links to resources used for these notes

* [Functional Programming Concepts](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)
* [Node JS Tutorial for Beginners #6 - Modules and require()](https://www.youtube.com/watch?v=xHLd36QoS4k)
* Chat GPT
