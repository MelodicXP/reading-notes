# 401 - Class 03 - Express REST API

## Why This Topic Matters

ES6 Classes are a fundamental concept in modern JavaScript, crucial for structuring and organizing complex applications. They provide a clear, concise, and more understandable way to create objects and deal with inheritance, making the code more maintainable and scalable. Understanding ES6 classes is essential for any JavaScript developer, as they are widely used in front-end frameworks like React and back-end frameworks like Node.js. Their introduction marked a significant step towards more robust and object-oriented JavaScript, aligning it with other programming languages that use class-based structures, thus easing the learning curve for developers from different programming backgrounds.

## Review ES6 Classes

1. **Classes are a template for creating ______.**
   Objects. Classes in JavaScript provide a blueprint for creating multiple objects with the same structure and methods.

2. **Can a class declaration be hoisted?**
   No, class declarations are not hoisted. Unlike function declarations, you need to define a class before you can use it. It's similar to needing a recipe before you can start cooking.

3. **How would you describe a constructor and contextual “this” to a non-technical friend?**
   A constructor is like the initialization instructions for a new gadget. When you create an object from a class (think of the class as a gadget blueprint), the constructor is the part that sets up your new object with all the initial settings and data it needs to start functioning.

   The contextual “this” refers to the current object you are working with. Imagine you are a teacher in a classroom; when you talk about "this student," you're referring to a specific student you are currently dealing with or pointing to. In JavaScript, “this” helps you refer to specific properties or methods of the object you're currently working on.

## Using Express Routing

1. **Within Express, what does routing refer to?**

   Routing in Express refers to determining how an application responds to a client request to a particular endpoint, which is a URI (or path) and a specific HTTP request method (GET, POST, etc.). Each route can have one or more handler functions, which are executed when the route is matched. Routing is essentially the way Express apps respond to different client requests based on the URL and HTTP method used.

2. **What is the difference between a route path and a route method?**

   - **Route Path:** The route path is a part of the URL that determines which endpoint the request is made to. It's like the address of a house. For example, in `app.get('/about', ...)` the `/about` is the route path.

   - **Route Method:** The route method corresponds to an HTTP method. It defines the type of action the client wants to perform and how the server should respond. It's like saying whether you want to 'view' (GET), 'create' (POST), 'update' (PUT), or 'delete' (DELETE) something at that address. In the same example, `get` is the route method.

3. **When is it appropriate to add `next` as a parameter to a route handler and what must you do if `next` has been passed to your middleware as a parameter?**

   - `next` is added as a parameter to a route handler when you want to pass control to the next middleware function in the Express application. It's used when the current middleware does not end the request-response cycle but instead passes control to the next middleware function.

   - If `next` is used, and there is an error or you want to skip to the next middleware, you call `next()` with an error argument (if any). If you don't call `next()`, the request will be left hanging or stalled. For example, in an error handling situation, you might use `next(new Error('custom error'))` to pass control to the error-handling middleware.

## Express Routing

1. **What is an Express Router?**
   The Express Router is a mini-application in Express which allows you to manage routes and endpoints in a modular and flexible way. It is like a 'mini-Express application' dedicated solely to handling routes. Using Router, you can create route handlers, and it enables the separation of route management for different parts of your application, making the code more modular and maintainable.

2. **By what means do we initialize `express.Router()` in an Express server?**
   To initialize `express.Router()`, you first need to import Express and then use the `.Router()` method. Here's a basic example:

   ```javascript
   const express = require('express');
   const router = express.Router();
   ```

3. **What do we use route middleware for?**  

   Route middleware in Express is used to run specific code or functions when certain routes are hit. It can be used for a variety of purposes such as:

   - Executing code to process the data before reaching the route handler (logging).
   - Making changes to request and response objects.
   - Ending request-response cycle.
   - Calling next middleware in the stack.
   - Performing authentication and authorization checks.
   - Handling errors or specific conditions in a route.
   - Middleware functions have access to the request object (req), the response object (res), and the next function in the application’s request-response cycle.

## Links to resources used for these notes

- [Review: ES6 Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
- [Using Express Routing](https://expressjs.com/en/guide/routing.html)
- [Express Routing](https://www.digitalocean.com/community/tutorials/learn-to-use-the-new-router-in-expressjs-4)
- Chat GPT
