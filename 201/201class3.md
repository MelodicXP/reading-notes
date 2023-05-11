# 201 - Class 3 - Lists, The Box Model, and Loops

## Continue Reading - Learn HTML

1. **When should you use an unordered list in your HTML document?**  
For grouping a collection of items that do not have a numerical ordering, and their order in the list is meaningless. Typically, unordered-list items are displayed with a bullet, which can be of several forms, like a dot, a circle, or a square.  

2. **How do you change the bullet style of unordered list items?**  
The bullet style is not defined in the HTML description of the page, but in its associated CSS, using the *list-style-type property*.  

3. **When should you use an ordered list vs an unordered list in your HTML document?**  
When the order is meaningful, such as steps in a recipe, turn-by-turn directions, and list of ingredients in decreasing proportion on nutrition informationa labels.

4. **Describe two ways you can change the numbers on list items provided by an ordered list?**  
    1. Using *type="i"* attribute for Roman Numeral type.
    2. Using the *"start = 4"* attribute so that numbers can start at desired beginning point, such as wanting list to start at number the number four.

## Learn CSS  

1. **Describe the CSS properties of margin and padding as characters in a story. What is their role in a story titled: “The Box Model”?**  
Mr. Padding protects the main character of the story named Content by pushing all the walls surrouding it away or closer together as needed.  
Mrs. Margin protects the house Content lives by using all her powers to push away any other intruders that want to come within a certain distance of Content's home.  

2. **List and describe the four parts of an HTML elements box as referred to by the box model.**  
    1. Content box: The area where your content is displayed; size it using properties like *inline-size* and *block-size* or *width* and *height*.
    2. Padding box: The padding sits around the content as white space; size it using *padding* and related properties.
    3. Border box: The border box wraps the content and any padding; size it using *border* and related properties.
    4. Margin box: The margin is the outermost layer, wrapping the content, padding, and border as whitespace between this box and other elements; size it using *margin* and related properties.  

## Learn JS

1. **What data types can you store inside of an Array?**  
An array can store various data types — strings, numbers, objects, and even other arrays. We can also mix data types in a single array — we do not have to limit ourselves to storing only numbers in one array, and in another only strings.  
An array can store a list of data items under a single variable name. Generally described as "list-like objects"; they are basically single objects that contain multiple values stored in a list.  

2. **Is the people array a valid JavaScript array? If so, how can I access the values stored? If not, why?**  
The array below is a valid. One example of how to access the values stored in the array is via a *console.log(people\[0\])* which would output *'pete'*.

    ```ruby
    const people = [  
      ['pete', 32, 'librarian', null],  
      ['Smith', 40, 'accountant', 'fishing:hiking:rock_climbing'],  
      ['bill', null, 'artist', null]  
    ]; 
    ```

3. **List five shorthand operators for assignment in javascript and describe what they do.**  
    1. Addition assignment: *x += f()* same thing as ---> *x = x + f()*
    2. Subtraction assignment: *x -= f()* same thing as ---> *x = x - f()*
    3. Multiplication assignment: x *= f()* same thing as ---> *x = x \* f()*
    4. Division assingment: *x /= f()* same thing as ---> *x = x / f()*
    5. Remainder assignment: *x %= f()* same thing as ---> *x = x % f()*

4. **Read the code below and evaluate the last expression and explain what the result would be and why.**  
The last expression in the code below would evaluate to:  
***'10dog'*** (skips the boolean in the expression and concatenates a and c variable).

    ```ruby
    let a = 10;  
    let b = 'dog';  
    let c = false;

    // evaluate this  
    (a + c) + b;
    ```

5. **Describe a real world example of when a conditional statement should be used in a JavaScript program.**  
In a game if the player's number of lives reaches zero, then via conditional inform that the game is over.  

6. **Give an example of when a Loop is useful in JavaScript.**  
A loop is useful in outputting data from an array so that it can keep looping through and pull the data needed in each pass.

## Links to resources used for these notes

* [Learn HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
* [Ordered List](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ol)
* [Unordered List](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/ul)
* [Learn CSS](https://developer.mozilla.org/en-US/docs/Learn/CSS)
* [The Box Model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)
* [Learn JS](https://developer.mozilla.org/en-US/docs/Learn/JavaScript)
* [Arrays](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/Arrays)
* [Operators and Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators)
* [Conditionals](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals)
* [Loops](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Looping_code)
