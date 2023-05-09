# 201 Class 1 - Introduction to Web Development

## Continue Reading - Introduction to HTML

1. **Why is it important to use semantic elements in our HTML?**  
Semantics are relied on everywhere. We rely on previous experience to tell us what the function of an everyday object is; when we see something, we know what its function will be. In a similar way, we need to make sure we are using the correct HTML elements, giving our content the correct meaning, function, or appearance.  
The *\<h1>* element is a semantic element, which gives the text it wraps around the role (or meaning) of "a top level heading on your page." The semantic value will then be used in multiple ways, for example by search engines and screen readers.

2. **How many levels of headings are there in HTML?**  
There are six levels of headings in HTML *(h1, h2, h3, h4, h5, and h6)*  

3. **What are some uses for the *\<sup>* and *\<sub>* elements?**  
When marking up items like dates, chemical formulae, and mathematical equations so they have the correct meaning.  

4. **When using the *\<abbr>* element, what attribute must be added to provide the full expansion of the term?**  
The *title* attribute.

## Learn CSS

1. **What are ways we can apply CSS to our HTML?**
    * External stylesheet
    * Internal stylesheet
    * Inline styles  
    &nbsp;
2. **Why should we avoid using inline styles?**  
First, it is the least efficient implementation of CSS for maintenance. One styling change might require multiple edits within a single web page. Second, inline CSS also mixes (CSS) presentational code with HTML and content, making everything more difficult to read and understand. Separating code and content makes maintenance easier for all who work on the website.  

3. **Review the block of code below and answer the following questions:**
    1. What is representing the selector?  
    The *h2* represents the selector which in this case is selecting the *h2* elements.  

    2. Which components are the CSS declarations?  
    The pairing of a property and a value is called the *CSS declaration* which in this case one fo the delclarations would be *'color:black;'*  

    3. Which components are considered properties?
    *'color'*, and *'padding':* are the properties.  

          *h2 {  
          color: black;  
          padding: 5px;  
          }*  

## Learn JS

1. **What data type is a sequence of text enclosed in single quote marks?**  
A string data type.  

2. **List 4 types of JavaScript operators.**  
    1. Addition operator: *'+'*
    2. Assignment operator: *'='*
    3. Strictly equality: *'==='*
    4. Does-not-equal: *'!=='*  

&nbsp;
3. **Describe a real world Problem you could solve with a Function.**  
A real world problem that coul be solved with a function is making a function to use as a basic template for my strucutring my notes in these classes.  I tend to use the same struture repeatedly, so a function that can automatically make my structure in my .md reading notes files would be useful!

## Making Decisions In Your Code - Conditionals

1. An if statement checks a **CONDITION** and if it evaluates to **TRUE**, then the code block will execute.  

2. **What is the use of an else if?**  
    * Else if allows for more choices/outcomes.  
    * A typical if/else statement provides two choices/outcomes.  
    * Using an else if allows to chain on extra choices/outcomes.  
&nbsp;
3. **List 3 different types of comparison operators.**  
    1. *'==='* - tests if value is identical to another
    2. *'>'* - tests if value is greater than another
    3. *'>='* - tests if one value is greater than or equal to another.  
&nbsp;
4. **What is the difference between the logical operator '&&' and '\|\|'?**  
    * *'&&'* - *'And operator'*, both conditions must evaluate to to true.  
    * *'\|\|'* - *'OR operator'*, only one of the conditions must evaluate to true.

## Links to resources used for these notes

* [HTML Text Fundamentals](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/HTML_text_fundamentals)
* [HTML Advanced Text Formatting](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting)
* [How CSS is Structured](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_is_structured)
* [JavaScript Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics)
* [Making Decisions in YOur Code - Conditionals](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/conditionals)
