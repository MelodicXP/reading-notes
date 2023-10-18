# 301 - Class 8 - APIs

## Why this topic matters  

  This topic matters as it allows to know the proper verbs to use when dealing with GET, POST, PUT, PATCH, and DELETE.

## API Design Best Practices

1. **What does REST stand for?**

    Representational State Transfer.

2. **REST APIs are designed around a ____.**

    Resource. Which IS any kind of object, data, or service that can be accessed by the client.

3. **What is an identifier of a resource? Give an example.**  

    A URI that uniquely identifies that resource. For example, the URI for a particular customer order might be: https:\//adventure-works.com/orders/1

4. **What are the most common HTTP verbs?**

    GET, POST, PUT, PATCH, and DELETE.

5. **What should the URIs be based on?**  

    When possible, resource URIs should be based on nouns (the resource) and not verbs (the operations on the resource).  

6. **Give an example of a good URI.**  

    https:\//adventure-works.com/orders // Good  
    https:\//adventure-works.com/create-order // Avoid

7. **What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?**  

    Web requests impose a load on the web server. The more requests, the bigger the load.Web APIs that expose a large number of small resources. Such an API may require a client application to send multiple requests to find all of the data that it requires. Instead,  denormalize the data and combine related information into bigger resources that can be retrieved with a single request.

8. **What status code does a successful GET request return?**  

    A successful GET method typically returns HTTP status code 200 (OK).

9. **What status code does an unsuccessful GET request return?**  

    If the resource cannot be found, the method should return 404 (Not Found).

10. **What status code does a successful POST request return?**  

    If a POST method creates a new resource, it returns HTTP status code 201 (Created).

11. **What status code does a successful DELETE request return?**  

    If the delete operation is successful, the web server should respond with HTTP status code 204 (No Content), indicating that the process has been successfully handled, but that the response body contains no further information.

## Links to resources used for these notes

* [API Design Best Practices](https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design)
* Chat GPT
