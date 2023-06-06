# 201 - Class 08 - Layout with CSS

## Learn CSS Flexbox

1. **Flexbox is designed for one-dimensional content. Explain what this means.**  

    [Found information here](https://tutorial.techaltum.com/css-flexbox.html)

    This means that with flexbox You can control alignment in one axis, a row or a column, not both together as we can do in grid.  
    When a flex container wraps it creates multiple flex lines. In terms of space distribution, each line acts like a new flex container. Therefore if you are wrapping rows, it is not possible to get something in row 2 to line up with something above it in row 1.  
    The flex box is CSS Layout Design built using the display:flex property. For two-dimensional layouts, use CSS Grids that can handle both row and column.

2. **Explain the difference between the main axis and cross axis.**

    The main axis is the one set by the flex-direction property. If the flex-direction property is 'row', the main axis is along the row, and if it is 'column' the main axis is along the column.  Flex items move as a group on the main axis.  
    The cross axis runs in the other direction perpendicular to the main axis, so if flex-direction is 'row' the cross axis runs along the 'column'.

    You can do two things on the cross axis:

    1. You can move the items individually or as a group, so they align against each other and the flex container.
    2. If wrapped flex lines are present, those lines can be treated as a group to control how space is assigned to those lines.  

3. **How can using certain properties of flexbox negatively impact accessibility?**  
    The row-reverse and column-reverse values are a examples of how it can impact accessibility in a negative fashion. When using these values the reordering only happens for the visual order, not the logical order. This is important to understand as the logical order is the order that a screen reader will read out the content, and anyone navigating using the keyboard will follow.

## CSS Layout - Flexbox

1. **What are some advantages of using flexbox over float?**

    1. Better layout designs
    2. Advantage of flexible layouts.
    3. Supports IE 10 and above browsers.
    4. Auto height and width option available.
    5. Easy to change direction of flex columns.
    6. Vertically centering a block of content inside its parent.
    7. Making all the children of a container take up an equal amount of the available width/height, regardless of how much width/height is available.
    8. Making all columns in a multiple-column layout adopt the same height even if they contain a different amount of content.

2. **How does this topic connect with your long term goals?**

    It connects with my long term goals of learning software development because it’ll allow me the capability of modifying elements much easier and quicker in CSS.

## Links to resources used for these notes

* [Domain Modeling](https://github.com/codefellows/domain_modeling#domain-modeling)
* [HTML Table Basics](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics)
* [Introducing Constructors](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Objects/Basics#introducing_constructors)
* [Object Prototypes Using A Constructor](https://ui.dev/beginners-guide-to-javascript-prototype)
