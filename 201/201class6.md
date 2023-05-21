# 201 - Class 6 - Domain Modeling, Intro to the DOM, and Object Literal Notation

## JavaScript Object Basics

1. **How would you describe an object to a non-technical friend you grew up with?**  
Think of an object as box that contains items associated to each other.  For example, imagine a box labeled "kitchen stuff". Inside the box you might have spoons, plates, cups, cookware, etc... This is the technical definition: An object is a collection of related data and/or functionality. These usually consist of several variables and functions (which are called properties and methods when they are inside objects).  
2. **What are some advantages to creating object literals?**  
When you want to transfer a series of structured, related data items in some manner, for example sending a request to the server to be put into a database. Sending a single object is much more efficient than sending several items individually, and it is easier to work with than an array, when you want to identify individual items by name.  

3. **How do objects differ from arrays?**

    * The major difference is that an array stores the data in an ordered collection in which the data can be accessed using a numerical index. As a suggestion if you have to store the data in order or in a sequence then use array otherwise you can use object for everything else. [source of suggestion](https://learnersbucket.com/examples/array/what-is-the-difference-between-an-array-and-an-object-in-javascript/)

4. **Give an example for when you would need to use bracket notation to access an object’s property instead of dot notation.**  
 If an object property name is held in a variable, then you can't use dot notation to access the value, but you can access the value using bracket notation.  

5. **Evaluate the code below. What does the term 'this' refer to and what is the advantage to using 'this'?**

    * 'this' refers to the current object the code is being written inside.  It is useful if you create more than one object literal, 'this' enables you to use the same method definition for every object you create. Essential when we using constructors to create more than one object from a single object definition.

```javascript
const dog = {
  name: 'Spot',
  age: 2,
  color: 'white with black spots',
  humanAge: function (){
  console.log(`${this.name} is ${this.age*7} in human years`);
  }
}
```

## Introduction to the DOM

1. **What is the DOM?**  
The Document Object Model (DOM) is a programming interface for web documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects; that way, programming languages can interact with the page.  

2. **Briefly describe the relationship between the DOM and JavaScript.**  
JavaScript, but uses the DOM to access the document and its elements. The DOM is not a programming language, but without it, the JavaScript language wouldn't have any model or notion of web pages, HTML documents, SVG documents, and their component parts. The document as a whole, the head, tables within the document, table headers, text within the table cells, and all other elements in a document are parts of the document object model for that document. They can all be accessed and manipulated using the DOM and a scripting language like JavaScript.

* [JavaScript Object Basics](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics)
* [Introduction To The DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
* [Understanding the problem domain is the hardest part of programming](https://simpleprogrammer.com/solving-problems-breaking-it-down/)
* [What’s the difference between primitive values and object references in JavaScript?](https://betterprogramming.pub/intermediate-javascript-whats-the-difference-between-primitive-values-and-object-references-e863d70677b)
