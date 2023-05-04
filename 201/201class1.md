# 201 Class 1 - Setup Developer Toolbelt

## Statement why this topic matters as it relates to what you are studying in this module.  

This topic matters because it serves as a refresher to material covered in 102.  Futhermore it serves as a setup to the foundation upon which our projects will be built upon in the upcoming classes. It provides the fundamental information and resources needed in relation to HTML structure, elements, attributes, JavaScript variables, and more.

## Getting Started

1. **Compose a short poem describing how HTTP sends data between computers:**

   *&nbsp;&nbsp; HTTP defines the language spoken between a client and server*  
   *&nbsp;&nbsp; Its like the language used when placing an order*  
   *&nbsp;&nbsp; The browser sends server an HTTP request message*  
   *&nbsp;&nbsp; To send a copy of website to client, HTTP is impressive!*
&nbsp;
2. **Describe how HTML, CSS, and JS files are "parsed" in the browser:**  
 The files are parsed in the following order:

    * HTML file is parsed first by the browser, which browser uses to recognize any *\<link>* element references to external CSS style and any *\<script>* element references to scripts.
    * As browser parses the HTML, it sends requests back to server for any CSS files it has from *\<link>* elements, and then from those parses the **CSS** and **JavaScript.**  
&nbsp;
3. **How can you find images to add to a Website?:**  

    * Go to Google Images
    * Locate desired image
    * Right-click image and choose *'Save Image As...'*, save to safe place.  You may also copy image's web address for later use.
    * To reduce violating copyright use Google's license filter by clicking *Tools > Usage rights > Create Commons licenses*.  
&nbsp;
4. **How do you create a *'String'* vs a *'Number'* in JavaScript?**  
**Strings** are signified by enclosing text in single or double quotes:  
*Example: let myVariable = 'Bob';*  
**Numbers** do not use quotes.  
*Example: let myVariable = 10;*  
&nbsp;
5. **What is a *'Variable'* and why are they important in JavaScript?**  
Variables are containers that store values. These values if desired can be manipulated.  This allows you to do dynamic actions like personalize a greeting message or change an image displayed in an image gallery.

## Introduction to HTML

1. **What is an HTML attribute?**  
Attributes contain extra information about the element that won't appear in the content.  
An attribute should have:

    * A space between it and the element name. (For an element with more than one attribute, the attributes should be separated by spaces too.)
    * The attribute name, followed by an equal sign.
    * An attribute value, wrapped with opening and closing quote marks.  

2. **Describe the Anatomy of an HTML element.**  
    * Below is the anatomy of an HTML document:  
    *\<!DOCTYPE html>  
      \<html lang="en-US">  
        &nbsp;&nbsp;&nbsp;\<head>  
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\<meta charset="utf-8" />  
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\<title>My test page</title>  
        &nbsp;&nbsp;&nbsp;\</head>  
        &nbsp;&nbsp;&nbsp;\<body>  
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\<p>This is my page</p>
        &nbsp;&nbsp;&nbsp;\</body>  
        \</html>*  

3. **What is the Difference between *'\<article>'* and *'\<section>'* element tags?**  
    * *\<article>* element: Self-contained syndicatable or reusable composition  
    * *\<section>* element: Generic document or application section  

4. **What Elements does a “typical” website include?**  
    * **header:** \<header>.  
    * **navigation bar:** \<nav>.  
    * **main content:** \<main>, with various content subsections represented by \<article>, \<section>, and \<div> elements.  
    * **sidebar:** \<aside>; often placed inside \<main>.  
    * **footer:** \<footer>.  

5. **How does metadata influence Search Engine Optimization?**  
Specifying a description that includes keywords relating to the content of your page is useful as it has the potential to make your page appear higher in relevant searches performed in search engines (such activities are termed Search Engine Optimization, or SEO.)  

6. **How is the *'\<meta>'* HTML tag used when specifying metadata?**  
    * Metadata: (data about the HTML, such as the author, and important keywords that describe the document). It's data that describes data. For example, an HTML document is data, but HTML can also contain metadata in its *\<head>* element that describes the document — for example who wrote it, and its summary.  
    *Example: \<meta charset="utf-8" />*  

## How to start to design a Website

1. **What is the first step to designing a Website?**  
*Project ideation* is the first step when creating a website. When you get an idea and want to turn it into a website, there are a few questions you should answer before anything else:
    * What exactly do I want to accomplish?
    * How will a website help me reach my goals?
    * What needs to be done, and in what order, to reach my goals?  

2. **What is the most important question to answer when designing a Website?**  
The most important question is "What exactly do I want to accomplish?"

## Semantics

1. **Why should you use an *'\<h1>'* element over a *'\<span>'* element to display a top level heading?**  
The *\<h1>* element should be used because it gives the text it wraps around the role (or meaning) of "a top level heading on the page." A *\<span>* element may look like an *\<h1>* element but will not be given any role or meaning  

2. **What are the benefits of using semantic tags in our HTML?**

    Some of the benefits from writing semantic markup are as follows:
    * Search engines will consider its contents as important keywords to influence the page's search rankings
    * Screen readers can use it as a signpost to help visually impaired users navigate a page
    * Finding blocks of meaningful code is significantly easier than searching through endless divs with or without semantic or namespaced classes
    * Suggests to the developer the type of data that will be populated
    * Semantic naming mirrors proper custom element/component naming

## What is JavaScript?

1. **Describe 2 things that *require* JavaScript in the Browser?**  
    * Storing useful values inside variables.
    * Operations on pieces of text.  

2. **How can you add JavaScript to an HTML document?**
Via the \<script> element. JavaScript is applied to your HTML page in a similar manner to CSS. Whereas CSS uses \<link> elements to apply external stylesheets and \<style> elements to apply internal stylesheets to HTML, JavaScript only needs the \<script> element.

## Links to resources used for these notes

* [How the web works](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works)
* [Website design and process](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/What_will_your_website_look_like)
* [JavaScript basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/JavaScript_basics)
* [Introduction to HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML)
* [Getting started with HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started)
* [HTML Structure](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure)
* [Metadata in HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML)
* [How to start to design a website](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Design_and_accessibility/Thinking_before_coding)
* [Semantics](https://developer.mozilla.org/en-US/docs/Glossary/Semantics)
* [What is JavaScript?](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript)
