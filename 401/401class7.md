# 401 - Class 07 - Bearer Authorization

## Why This Topic Matters  

  Authentication matters because it's the digital equivalent of a lock on your front door, ensuring that only authorized users can access sensitive information or perform certain actions online. It protects both user data and system integrity from unauthorized access, thereby maintaining privacy and security in an increasingly interconnected world. Without effective authentication, systems are vulnerable to breaches and misuse, leading to potential financial loss, data theft, and erosion of trust among users and clients.

## Intro to JWT

1. **What is a JSON Web Token (JWT)?**  

    According to the reading, a JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

2. **When should we use JSON Web Tokens?**  

    According to the reading:

    **Authorization:** This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used across different domains.

    **Information Exchange:** JSON Web Tokens are a good way of securely transmitting information between parties. Because JWTs can be signed—for example, using public/private key pairs—you can be sure the senders are who they say they are. Additionally, as the signature is calculated using the header and the payload, you can also verify that the content hasn't been tampered with.

3. **Claims are expected in which structural component of a JWT?**  
    **Payload**  
    The second part of the token is the payload, which contains the claims. Claims are statements about an entity (typically, the user) and additional data. There are three types of claims: registered, public, and private claims.  

    ``` javascript
    {
      "sub": "1234567890",
      "name": "John Doe",
      "admin": true
    }
    ```

## Are JWTs Secure?

1. **If I get a JWT and I can decode the payload, how can we call that secure?**  

    JWTs can be either signed, encrypted or both. If a token is signed, but not encrypted, everyone can read its contents, but when you don't know the private key, you can't change it. Otherwise, the receiver will notice that the signature won't match anymore.

    The header and payload are encoded, not encrypted, which means their contents can be easily decoded. However, the signature part is where the security magic happens.

    The signature is created by taking the encoded header, the encoded payload, a secret (known only to the server), and running them through a cryptographic hash function. This signature ensures that the content (header and payload) hasn't been tampered with. Only parties with the correct secret can verify the signature and trust the token's integrity. If an attacker tries to modify either the header or the payload, they would need to regenerate the signature using the secret, which they should not have access to.

    JWTs do not aim to hide the payload data. If you need to keep the payload data confidential, you should encrypt it before adding it to the JWT. The primary security feature of JWTs is to ensure data integrity and authenticity: verifying that the data comes from a trusted source and has not been altered in transit.

    JWTs can be considered secure because even though the payload can be decoded, the integrity and authenticity of the token can be verified through the signature. Unauthorized parties cannot modify the token without access to the secret used to create the signature, and thus cannot forge valid tokens.

2. **If sending a JWT, what must sender and receiver both know? Hint, it’s appended in the signature.**

    When sending a JWT, both the sender and the receiver must know the secret key that is used to create and verify the JWT's signature.

3. **Explain how concatenated content and secret can be sent and received securely to a non-technical recruiter.**
    Imagine you have a secret box where you can safely put messages inside, and you have a special key to lock it. Now, you want to send a message to someone in a way that ensures nobody else can read it or tamper with it during delivery. Here's how you can do it securely, similar to how concatenated content (like a message) and a secret (like a password or key) work together in technology:

    Writing the Message: You write your message and place it inside the box. In the digital world, this message is like the content you want to send securely.

    Using the Secret Key: You lock the box with your special key. This key is a secret that only you and the intended recipient know. In digital security, this is similar to encrypting data using a secret key or password.

    Sending the Box: You send the locked box to your friend. Even if someone intercepts the box while it's being delivered, they can't open it without the key. This is akin to sending encrypted data over the internet; it's secure because without the secret key, the data is unreadable.

    Receiving and Opening the Box: Your friend receives the box. Since they know the secret key (maybe you shared it with them earlier in a secure way), they can unlock the box and read the message. In the context of digital communication, this means the recipient uses the shared secret to decrypt the data, making it readable again.

    The key point here is that the security of the message depends on keeping the key secret and only sharing it through secure means. This ensures that even if someone gets their hands on the box (or the encrypted data), without the key, they can't access the message inside. This way, the content and the secret are securely sent and received, ensuring privacy and security in the communication.

## JWTs Explained

1. **Why use JWT?**  
    Compact
      JWT can be senti via URL, POST request, HTTP Header
      Fast Transmission
    Self-contained
      Contains information about the user
      Avoiding querying the database more than once.

2. **JWT is Compact and self-contained. Describe how this is useful to a non-technical friend.**  

3. **What are the three components (the structure) of a JWT signature?**  

    Header 'aaaa' part - contains algorithm used like HMACSHA256 or RSA, establishes the type of token (JWT).  The header is Base64Url encoded to form the first part.

    ``` javascript
      {
        "alg": "HS256",
        "typ": "JWT"
      }
    ```

    Payload 'bbbb' part - contains claims, which are user details or additional metadata. Payload is then Base64Url encoded to form the second part

    ``` javascript
      {
        "sub": "123456789",
        "name": "John Doe",
        "admin": true
      }
    ```

    Signature 'cccc' part - Combines base64 Header and base64 Payload with secret. The signature is used to secure the token and verify that the sender of the JWT is who it says it is and to ensure that the message wasn't changed along the way. To create the signature, you take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that. The signature is the third part of the JWT.

    ``` javascript
      HMACSHA256(
        base64UrlEncode(header) + "."+
        base64UrlEncode(payload),
        secret
      )
    ```

    In essence, a JWT is structured as follows: [Base64Url encoded header].[Base64Url encoded payload].[Signature]. The header and payload are simply encoded, not encrypted, meaning they can be read by anyone. However, altering them without knowing the secret is impossible, thanks to the signature.

## Links to resources used for these notes

* [Intro to JWT](https://jwt.io/introduction/)
* [Are JWTs Secure?](https://stackoverflow.com/questions/27301557/if-you-can-decode-jwt-how-are-they-secure)
* [JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo)
* Chat GPT
