# 301 - Class 4 - React and Forms

## Why this topic matters  

  This topic matters is it allows for the implementation of forms and how to handle the state once data is input in a form.

## React Docs - Forms

1. **What is a ‘Controlled Component’?**  

    A controlled componenet is a form element in React (input or text area).  The input the form receives is managed with component's state.

2. **Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.**  

    Update responses as soon as entered.  It allows for real-time feedback and validation such as verifying if email is valid or password meets criteria.  This enhances the user experience as it gives them guidenace in real-time.  Data perisistence is another reason.  If user accidentally closes browser data won't be lost.  

    There needs to be balance though. If a form involves making frequent server requests or involves very complex validation,  debouncing or validating data maybe be preferable before updating the state.  It an be especially helpful when dealing with functions like search suggestions or handling rapid user inputs.

3. **How do we target what the user is entering if we have an event handler on an input field?**  

   'event.target.value' - Target what the user is entering into an input field by using the event object passed into event handler function. The event object contains information about the event, including the current value of the input field.  See code example below:

   ``` javascript
    <input
      type="text"
      value={this.state.inputValue}
      onChange={this.handleInputChange}
    />
   ```

   ``` javascript
    handleInputChange(event) {
      // Access user's input value using 'event.target.value'
      const userInput = event.target.value;
      
      // Now can use userInput as needed, e.g., store it in state
      this.setState({ inputValue: userInput });
    }
   ```

    Within handleInputChange function can access what user is entering by using event.target.value. This property contains current value of input field.

    * _event:_ The event object contains various properties and methods related to the event.

    * _target:_ refers to the element that triggered the event, in this case, the input field.

    * _value:_ is a property of the input element, which represents its current value.  

    By following this pattern, user input is captured as user type in input field. The inputValue in component's state is updated with each keystroke, making it available for further processing or rendering in component.

## The Conditional (Ternary) Operator Explained

1. **Why would we use a ternary operator?**

    It is a concise way to write conditional statements. It's a shortcut for making decisions in code based on a condition.  
    The ternary operator consists of three parts:  

    * a condition
    * a question mark ? - an expression to execute if condition is true
    * colon : to specify the expression to execute if condition is false

2. **Rewrite the following statement using a ternary statement:**

  ``` javascript
    if(x===y){
      console.log(true);
    } else {
      console.log(false);
    }
  ```

  ``` javascript
    x === y ? console.log(true) : console.log(false);
  ```

## Links to resources used for these notes

* [React Bootstrap - Forms](https://react-bootstrap.netlify.app/docs/forms/overview/)
* [React Docs - conditional rendering](https://legacy.reactjs.org/docs/conditional-rendering.html)
* ChatGPT
