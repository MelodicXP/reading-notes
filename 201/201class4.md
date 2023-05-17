# 201 - Class 4 - Links, Layouts, and Functions

## Creating Hyperlinks

1. **To create a basic link, we wrap text or other content inside what element?**  
The text is wrapped inside the \<a\> element.  

2. **The href attribute contains what information?**  
It contains the web address.  

    ```html
    <p>
      I'm creating a link to
      <a href="https://www.mozilla.org/en-US/">the Mozilla homepage</a>.
    </p>
    ```

3. **What are some ways we can ensure links on our pages are accessible to all readers?**  
    * Use clear link wording
      * Don't repeat the URL as part of the link text — URLs look ugly, and sound even uglier when a screen reader reads them out letter by letter.
      * Don't say "link" or "links to" in the link text — it's just noise. Screen readers tell people there's a link. Visual users will also know there's a link, because links are generally styled in a different color and underlined (this convention generally shouldn't be broken, as users are used to it).
      * Keep your link text as short as possible — this is helpful because screen readers need to interpret the entire link text.
      * Minimize instances where multiple copies of the same text are linked to different places. This can cause problems for screen reader users, if there's a list of links out of context that are labeled "click here", "click here", "click here".
    * Leave clear sign posts when linking to non-HTML resources
      * If you're on a low bandwidth connection, click a link, and then a multiple megabyte download starts unexpectedly.

      ```html
      <p>
      <a href="https://www.example.com/large-report.pdf">
        Download the sales report (PDF, 10MB)
      </a>
      </p>

      <p>
      <a href="https://www.example.com/video-stream/" target="_blank">
        Watch the video (stream opens in separate tab, HD quality)
      </a>
      </p>
      ```

    * Use the download attribute when linking to a download

      ```html
      <a
        href="https://download.mozilla.org/?product=firefox-latest-ssl&os=win64&lang=en-US"
        download="firefox-latest-64bit-installer.exe">
        Download Latest Firefox for Windows (64-bit) (English, US)
      </a>
      ```

## CSS Layout: Normal Flow CSS Layout: Positioning

1. **What is meant by “normal flow”?**
The way that webpage elements lay themselves out if you haven't changed their layout.  

2. **What are a few differences between block-level and inline elements?**  
    * A block-level element's content fills the available inline space of the parent element containing it, growing along the block dimension to accommodate its content. y default, block-level elements are laid out in the block flow direction, which is based on the parent's writing mode (initial: horizontal-tb). Each element will appear on a new line below the last one, with each one separated by whatever margin that's been specified. In English, for example, (or any other horizontal, top to bottom writing mode) block-level elements are laid out vertically.  

    * The size of inline-level elements is just the size of their content. You can set width or height on some elements that have a default display property value of inline, like \<img\>, but display value will still remain inline.  
    Inline elements behave differently. They don't appear on new lines; instead, they all sit on the same line along with any adjacent (or wrapped) text content as long as there is space for them to do so inside the width of the parent block level element. If there isn't space, then the overflowing content will move down to a new line.

3. **___ positioning is the default for every html element.**  
Static positioning is the default that every element gets. It just means "put the element into its normal position in the document flow — nothing special to see here."  

4. **Name a few advantages to using absolute positioning on an element.**  
An absolutely positioned element no longer exists in the normal document flow. Instead, it sits on its own layer separate from everything else. Allows for creation of isolated UI features that don't interfere with the layout of other elements on the page. For example, popup information boxes, control menus, rollover panels, UI features that can be dragged and dropped anywhere on the page, and so on.  

5. **What is a key difference between fixed positioning and absolute positioning?**  

* Absolute positioning fixes an element in place relative to its nearest positioned ancestor (the initial containing block if there isn't one).  
* Fixed positioning usually fixes an element in place relative to the visible portion of the viewport.  
This means can create useful UI items that are fixed in place, such as persistent navigation menus that are always visible no matter how much the page scrolls.

## Functions – Reusable Blocks of Code

1. Describe the difference between a function declaration and a function invocation.  

    * Function declaration - use the word function followed by name of function followed by parenthesis.  Allow to store a piece of code that does a single task inside a defined block, and then call that code whenever needed by using a single short command — rather than having to type out the same code multiple times.
    * Function invocation - accomplished by including the name of the function in the code somewhere, followed by parentheses.  

2. What is the difference between a parameter and an argument?

    * Parameter - placeholder names for the values that need to be included inside the function parentheses when declaring the function.
    * Argument - is the actual value that gets passed in the 'parameters' of the function when invoked.

## 6 Reasons for Pair Programming

1. Pick 2 benefits to pair programming and reflect on how these benefits could help you on your coding journey.
    * Greater efficiency - while taking a bit longer, will reduce time on the back-end as the output is higher quality code with less bugs and troubleshooting required otherwise.
    * Social skills - helps promote collaboration with others and their working styles.

## Links to resources used for these notes

* [Creating Hyperlinks](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Creating_hyperlinks)
* [CSS Layout: Normal Flow](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow)
* [CSS Layout: Positioning](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Positioning)
* [Functions – Reusable Blocks of Code](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Functions)
* [6 Reasons for Pair Programming](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)
