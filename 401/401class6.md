# 401 - Class 06 - Authentication

## Why This Topic Matters  

  Authentication matters because it's the digital equivalent of a lock on your front door, ensuring that only authorized users can access sensitive information or perform certain actions online. It protects both user data and system integrity from unauthorized access, thereby maintaining privacy and security in an increasingly interconnected world. Without effective authentication, systems are vulnerable to breaches and misuse, leading to potential financial loss, data theft, and erosion of trust among users and clients.

## Securing Passwords

1. **Explain to a non-technical friend how you would safely hash and store a password.**  

    Imagine you have a super secret diary that you don't want anyone else to read. To keep it safe, you invent a secret code that changes the words into something else, so even if someone finds your diary, they can't understand it. Hashing a password is like turning it into that secret code. Whenever you write down your password (like when you're saving it somewhere safe), you first turn it into this secret code. This way, even if someone sneaky finds where you saved your password, all they see is the secret code, not the real password. And the cool part? There's no easy way to turn the code back into the password. So, it's super safe!

2. **What is Bcrypt?**  

    According to the article in the reading Bcrypt is an adaptive hash function based on the Blowfish symmetric block cipher cryptographic algorithm and introduces a work factor (also known as security factor), which allows you to determine how expensive the hash function will be.  

    Bcrypt is like a very special, very clever lock for your secrets. It's a tool that helps us turn passwords into those secret codes we talked about. But it's not just any tool; it's like a magic wand that makes sure the secret code is really, really hard to guess. It does this by scrambling the password in a very complex way and even lets us decide how strong we want the magic spell to be. This means that even the sneakiest of sneaks would have a super hard time trying to figure out the password from the secret code.

3. **Why might you use something like Bcrypt?**  

    The work factor value determines how slow the hash function will be, means different work factor will generate different hash values in different time span, which makes it extremely resistant to brute force attacks. When computers become faster next year we can increase the work factor to balance it out i.e. to make the attack slower.

    Let's say you're building a treehouse club, and you want a lock that's so good, even the cleverest puzzle-solvers can't easily break in. You'd use Bcrypt because:

    * Super Strong Locks: It makes the passwords turn into secret codes that are really hard to figure out, keeping your treehouse club super safe.
    * Adjustable Magic: You can change how powerful the magic is (this is like choosing how complex the scrambling is). So, if you think you need an even stronger lock because the puzzle-solvers are getting smarter, you can crank up the magic.
    * Trusty Guardian: It's been used by lots of people for a long time, proving it's really good at keeping secrets safe. Like having a trusted guard dog that's been protecting treehouses for years.

## Basic Auth

1. **What is Basic Authentication?**  

    Basic Authentication is like the simplest form of showing your ID to prove who you are on the web. It's straightforward: when a user tries to access a protected resource, the server asks for a username and password. This duo is then encoded (not encrypted) into a format called Base64 and sent over the internet tucked inside an HTTP header.

2. **What properties are necessary in the header of a Basic Auth request?**

    For a Basic Auth request, the essential property that needs to be included in the header is the Authorization header. Here's the breakdown of what it contains:

    **Authorization Type:** This part is simply the text Basic indicating that the request is using Basic Authentication.

    **Credentials:** This is a Base64-encoded string that represents the username and password, concatenated with a colon (:). So, if your username is MelodicCoder and your password is SuperSecret, you first combine them into MelodicCoder:SuperSecret and then encode that string with Base64.

    Putting it all together, your Authorization header for a Basic Auth request would look something like this:

    ``` javascript
    Authorization: Basic [Base64-encoded-credentials]
    ```

    For example, if MelodicCoder:SuperSecret is Base64 encoded to TWVsb2RpY0NvZGVyOlN1cGVyU2VjcmV0, the header would be:

    ``` javascript
    Authorization: Basic TWVsb2RpY0NvZGVyOlN1cGVyU2VjcmV0
    ```

3. **How are `username:password` in Basic Auth encoded?**  

    In Basic Authentication, the **username:password** pair is encoded using Base64 encoding.  

    1. **Concatenate Username and Password:** First, the username and password are joined together with a colon (:) between them. This forms a single string like username:password.

    2. **Encode with Base64:** This concatenated string is then encoded using Base64. Base64 encoding takes the input string, breaks it down into bytes, and then converts those bytes into a set of ASCII characters from a predefined set of 64 characters (hence the name Base64). This results in a string that's safe to include in HTTP headers.

## OWASP auth cheatsheet

1. **Define the authentication process to a non-technical recruiter.**  
    You're trying to enter a VIP lounge (a website) at a concert (the internet). Here's the authentication process simplified:

    1. **Showing Your ID (Username and Password):**  
    Just like how you'd show your ID to prove you're old enough to enter the lounge, you give the website your username and password. This is your way of saying, "Hey, I'm supposed to be here. I have an account."

    2. **The Bouncer Checks Your ID (Verification):**  
    The person at the door (the server) checks your ID against a guest list (a database of users). They're making sure you are who you say you are, just like how a website checks your login details to see if they match what's on file.

    3. **Getting a Hand Stamp (Session Token):**  
    Once the bouncer sees you're on the list, they give you a hand stamp. This stamp lets you come and go without showing your ID again. On a website, once you're verified, the server gives your computer a digital stamp, called a session token. This way, you don't have to log in every time you click a new page.

    4. **Enjoy the Lounge (Access Granted):**  
    With that stamp, you can now enjoy everything the VIP lounge offers, just like how you can access all the features of the website you logged into.

2. **How should your error messaging respond (both HTTP and HTML)? Why?**  

    **HTTP:**

    **User-Friendly Descriptions:**  
    Along with the status code, your server should send a brief, human-readable explanation in the response body. For instance, a 404 status code might come with "Sorry, the resource you're looking for cannot be found."

    **Error Handling Suggestions:**  
    Where applicable, provide suggestions for next steps. For a 401 (Unauthorized), you might include "Please check your login credentials and try again."

    **HTTP:**  

    **User-Centric Messages:**  
    Avoid technical jargon. Instead of "404 Not Found," how about "Oops! We can't seem to find the page you're looking for." It's less about the code and more about the conversation.

    **Navigation Options:**  
    Include links back to the homepage, search function, or help center. You're not just saying "Wrong way," you're offering a map back to the main road.

    **Consistent Branding:**  
    Keep the look and feel in line with the rest of your site. It reassures users that they're still in the right place, despite the hiccup.

    **Why Is This Approach Important?**

    **User Experience (UX):**  
    Good error messaging keeps users from feeling lost or frustrated. It turns errors into opportunities for engagement rather than dead-ends that might lead them to leave your site.

    **Security:**  
    Be careful not to give away too much information, especially with server errors (like the 500 Internal Server Error). Revealing specifics could inadvertently provide hints to potential attackers about vulnerabilities.

    **Helpfulness:**  
    By guiding users on what to do next, you're providing value even in the face of errors. It shows that you care about their experience from start to finish.

    **Search Engine Optimization (SEO):**  
    Properly handled error pages (like using the correct 404 status code for missing pages) help search engines understand your site better and can prevent them from indexing broken links.

## Links to resources used for these notes

* [Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)
* [Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)
* [OWASP auth cheatsheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)
* Chat GPT
