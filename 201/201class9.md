# 201 - Class 09 - Forms and Events

## HTML Forms

1. **Why are forms so important in web development?**  
Forms are used for collecting data from users, or allowing them to control a user interface. Web forms are one of the main points of interaction between a user and a website or application. Forms allow users to enter data, which is generally sent to a web server for processing and storage (see Sending form data later in the module), or used on the client-side to immediately update the interface in some way (for example, add another item to a list, or show or hide a UI feature).

2. **When designing a form, what are some key things to keep in mind when it comes to user experience?**  
It's important to remember that the bigger the form, the more risk of frustrating people and losing users. Keep it simple and stay focused: ask only for the data absolutely needed.

3. **List 5 form elements and explain their importance.**  
    1. **\<form>** : This element formally defines a form. It's a container element like a \<section> or \<footer> element, but specifically for containing forms; it also supports some specific attributes to configure the way the form behaves. All of its attributes are optional, **but it's standard practice to always set at least the action and method attributes** (The **action attribute** defines the location (URL) where the form's collected data should be sent when it is submitted and
    the **method attribute** defines which HTTP method to send the data with (usually get or post).)
    2. **\<label>**: represents a caption for an item in a user interface. Is usually associated with a form control such as an \<input> or \<textarea>. It is the formal way to define a label for an HTML form widget. This is the most important element if you want to build accessible forms — when implemented properly, screen readers will speak a form element's label along with any related instructions, as well as it being useful for sighted users.
    3. **\<input>** : is used to create interactive controls for web-based forms in order to accept data from the user; a wide variety of types of input data and control widgets are available, depending on the device and user agent. The \<input> element is one of the most powerful and complex in all of HTML due to the sheer number of combinations of input types and attributes.
    4. **\<textarea>** : represents a multi-line plain-text editing control, useful when you want to allow users to enter a sizeable amount of free-form text, for example a comment on a review or feedback form.
    5. **\<button>** : allows the user to send, or "submit", their data once they have filled out the form.

## Learn JS

1. **How would you describe events to a non-technical friend?**  
Think of it like a school assembly event that has annoucements during the assembly. Throughout the assembly different 'events' take place such as teachers and speakers giving speeches, and the children giving a performance.  The school assembly represents the web page, and the speeches and performances represent the events in JavaScript.  When the time for a speech happens (event), the associated individual(s) get up and perform the response. In the same way when an event is triggered in Javascript, the associated code runs in response to the event.(which would be called the event handler).
2. **When using the addEventListener() method, what 2 arguments will you need to provide?**  
A 'type' argument that is a case-sensitive string representing the event type to listen for and 'listener object' argument which is the object that receives a notification when an event of the specificed type occurs.

3. **Describe the event object. Why is the target within the event object useful?**
The event object is automatically passed to event handlers to provide extra features and information. The target property of the event object is always a reference to the element the event occurred upon. Its useful for instance in the even of setting a random background color on a button rather than the whole page.  

4. **What is the difference between event bubbling and event capturing?**  
**Event bubbling** describes how the browser handles events targeted at nested elements. The events bubble up from the innermost element that was clicked.  
**Event capture** is like event bubbling but the order is reversed: so instead of the event firing first on the innermost element targeted, and then on successively less nested elements, the event fires first on the least nested element, and then on successively more nested elements, until the target is reached. Event capture is disabled by default. To enable it you have to pass the capture option in addEventListener().

## Links to resources used for these notes

* [HTML Forms](https://developer.mozilla.org/en-US/docs/Learn/Forms)
* [Your First Web Form](https://developer.mozilla.org/en-US/docs/Learn/Forms/Your_first_form)
* [How to Structure a Web Form](https://developer.mozilla.org/en-US/docs/Learn/Forms/How_to_structure_a_web_form)
* [Learn JS](https://developer.mozilla.org/en-US/docs/Learn/JavaScript)
* [Introduction to Events](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events)
* [HTML 5 Input Types](https://developer.mozilla.org/en-US/docs/Learn/Forms/HTML5_input_types)
* [Event Reference and listings](https://developer.mozilla.org/en-US/docs/Web/Events)
