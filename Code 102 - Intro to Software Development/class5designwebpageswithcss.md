# Class 5 - Design Web Pages with CSS

## What is the purpose of CSS?

* A language for specifying how documents are presented to users — how they are styled, laid out, etc.  
* Can be used for very basic document text styling — for example, for changing the color and size of headings and links.  
* Can be used to create a layout — for example, turning a single column of text into a layout with a main content area and a sidebar for related information. It can even be used for effects such as animation.

**Example:** - the main heading on the page will display as large red text (using the code below):

*h1 {  
  &nbsp;&nbsp;color: red;  
  &nbsp;&nbsp;font-size: 5em;  
}*

## What are the three ways to insert CSS into your project?

1. ***External CSS*** - With an external style sheet, change the look of an entire website by changing just one file. Each HTML page must include a reference to the external style sheet file inside the *'\<link>*' element, inside the *head section.*  
**Example:** External styles are defined within the *'\<link>*' element, inside the *'\<head>*' section of an HTML page:  
*\<!DOCTYPE html>  
\<html>  
\<head>  
&nbsp;&nbsp;**\<link rel="stylesheet" href="mystyle.css">**  
\</head>  
\<body>  
&nbsp;&nbsp;\<h1>This is a heading\</h1>  
&nbsp;&nbsp;\<p>This is a paragraph.\</p>  
\</body>  
\</html>*  
**Note:** An external style sheet can be written in any text editor, and must be saved with a .css extension. The external .css file should not contain any HTML tags.

2. ***Internal CSS***  
An internal style sheet may be used if one single HTML page has a unique style.  
The internal style is defined inside the *\<style>* element, inside the '*head section*'.  
**Example:**  
*\<!DOCTYPE html>  
\<html>  
\<head>  
\<style>  
&nbsp;&nbsp;&nbsp;&nbsp;**body {  
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;background-color: linen;  
    &nbsp;&nbsp;&nbsp;&nbsp;}  
&ensp;&ensp;h1 {  
    &nbsp;&nbsp;&ensp;&ensp;color: maroon;  
    &nbsp;&nbsp;&ensp;&ensp;margin-left: 40px;  
    &ensp;&ensp;}**  
\</style>  
\</head>  
\<body>  
&ensp;&ensp;\<h1>This is a heading\</h1>  
&ensp;&ensp;\<p>This is a paragraph.\</p>  
\</body>  
\</html>*

3. ***Inline CSS***  
An inline style may be used to apply a unique style for a single element.  
To use inline styles, add the style attribute to the relevant element. The style attribute can contain any CSS property.  
**Example:**  
*\<!DOCTYPE html>  
\<html>  
\<body>  
&ensp;&ensp;**\<h1 style="color:blue;text-align:center;">This is a heading\</h1>  
&ensp;&ensp;\<p style="color:red;">This is a paragraph.\</p>**  
\</body>  
\</html>*

## Write an example of a CSS rule that would give all \<p> elements red text

*p {  
    &ensp;&ensp;color: red;  
    }*
