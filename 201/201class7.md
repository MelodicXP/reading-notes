# 201 - Class 7 - HTML Tables and JS Constructor Functions

## Domain Modeling

1. **Explain why we need domain modeling.**  
Domain modeling is the process of creating a conceptual model for a specific problem. And a domain model that's articulated well can verify and validate your understanding of that problem. As a communication tool, it defines a vocabulary that can be used within and between both technical and business teams. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain.

## HTML Table Basics

1. **Why should tables not be used for page layouts?**  
    1. Layout tables reduce accessibility for visually impaired users: screen readers, used by blind people, interpret the tags that exist in an HTML page and read out the contents to the user. Because tables are not the right tool for layout, and the markup is more complex than with CSS layout techniques, the screen readers' output will be confusing to their users.
    2. Tables produce tag soup: As mentioned above, table layouts generally involve more complex markup structures than proper layout techniques. This can result in the code being harder to write, maintain, and debug.
    3. Tables are not automatically responsive: When you use proper layout containers (such as \<header>, \<section>, \<article>, or \<div>), their width defaults to 100% of their parent element. Tables on the other hand are sized according to their content by default, so extra measures are needed to get table layout styling to effectively work across a variety of devices.  

2. **List and describe 3 different semantic HTML elements used in an HTML \<table>.**  
    1. \<tr>  
    2. \<th>  
    3. \<td>

## Introducing Constructors

1. **What is a constructor and what are some advantages to using it?**  
A way to define the "shape" of an object — such as the set of methods and the properties it can have — and the advantage is that then you can create as many objects as desired, just by updating the values for the properties that are different.  
A constructor is just a function called using the 'new' keyword. When you call a constructor, it will:

    * create a new object
    * bind this to the new object, so you can refer to this in your constructor code
    * run the code in the constructor
    * return the new object.

2. **How does the term 'this' differ when used in an object literal versus when used in a constructor?**  
In object literals 'this' refers to the object itself.  With constructors 'this' refers to the newly created instance.  When using 'this' with a constructor it does not affect the object only the newly created instance by the constructor.

## Object Prototypes Using A Constructor

1. **Explain prototypes and inheritance via an analogy from your previous work experience.**  
Prototypes remind me of excel or word templates used in work.  The base template serves as the prototype.  Once any of us get a copy, the copy comes inheriting all of the prototype's traits. The copy can be modified with additional properties as needed for the situation while retaining all of the inherited properties and traits of the prototype.

## Links to resources used for these notes

* [Domain Modeling](https://github.com/codefellows/domain_modeling#domain-modeling)
* [HTML Table Basics](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics)
* [Introducing Constructors](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics#introducing_constructors)
* [Object Prototypes Using A Constructor](https://ui.dev/beginners-guide-to-javascript-prototype)
