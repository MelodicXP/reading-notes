# 201 - Class 5 - Images, Color, Text, and More Work With Functions

## HTML Media

1. **What is a real world use case for the 'alt' attribute being used in a website?**  
For use in situations where the image cannot be seen/displayed or takes a long time to render because of a slow internet connection. It is also good for accessbility purposes. See below for example:

    ```javascript
    <img
      src="images/dinosaur.jpg"
      alt="The head and torso of a dinosaur skeleton;
              it has a large head with long sharp teeth" />
    ```

    It can also be used for the following situations:  
    * The user is visually impaired, and is using a screen reader to read the web out to them. In fact, having alt text available to describe images is useful to most users.
    * As described above, the spelling of the file or path name might be wrong.
    * The browser doesn't support the image type. Some people still use text-only browsers, such as Lynx, which displays the alt text of images.
    * You may want to provide text for search engines to utilize; for example, search engines can match alt text with search queries.
    * Users have turned off images to reduce data transfer volume and distractions. This is especially common on mobile phones, and in countries where bandwidth is limited or expensive.  

2. **How can you improve accessibility of images in an HTML document?**
    * **Decoration.** You should use CSS background images for decorative images, but if you must use HTML, add a blank alt="". If the image isn't part of the content, a screen reader shouldn't waste time reading it.
    * **Content.** If your image provides significant information, provide the same information in a brief alt text – or even better, in the main text which everybody can see. Don't write redundant alt text. How annoying would it be for a sighted user if all paragraphs were written twice in the main content? If the image is described adequately by the main text body, you can just use alt="".
    * **Link.** If you put an image inside \<a\> tags, to turn an image into a link, you still must provide accessible link text. In such cases you may, either, write it inside the same \<a\> element, or inside the image's alt attribute – whichever works best in your case.
    * **Text.** You should not put your text into images. If your main heading needs a drop shadow, for example, use CSS for that rather than putting the text into an image. However, If you really can't avoid doing this, you should supply the text inside the alt attribute.  

3. **Provide an example of when the figure element would be useful in an HTML document.**
    * Express meaning in a compact, easy-to-grasp way.
    * Could go in several places in the page's linear flow.
    * Provide essential information supporting the main text.  

4. **Describe the difference between a gif image and an svg image, pretend you are explaining to an elder in your community.**  
    * **GIF (Graphics Interchange Format):** Good choice for simple images and animations. For example gifs are used in social media short "video" memes.
    * **SVG (Scalable Vector Graphics):** Vector image format; ideal for user interface elements, icons, diagrams, etc., that must be drawn accurately at different sizes. In other words its good for diagrams, icons, and other images which can be accurately drawn at any size. As such, SVG is popular for user interface elements in modern Web design.

5. **What image type would you use to display a screenshot on your website and why?**
Lossless WebP or PNG.  This is important if there's any text in your screenshot, as text easily becomes fuzzy and unclear under lossy compression.

## Learn CSS

1. **Describe the difference between foreground and background colors of an HTML element, pretend you are talking to someone with no technical knowledge.**  
    * Foreground color: represents the actual color of the content.  So in the example of text, it would color the actual text letters. To do this the 'color' property would be used.  
    * Background color: In the example of text, it would color the background behind the text, not the text itself. To do this the background-color property would be used.

2. **Your friend asks you to give his colorless blog website a touch up. How would you use color to give his blog some character?**  
By using color it could be used to color the text and itself and it would add color to any text decorations that might be used (such as under- or overlines, strike-through lines, and so forth ).  It could also be used to color the boxes and borders of text.

3. **What should you consider when choosing fonts for an HTML document?**  
Using websafe fonts for compatabiity across different the most used operating systems.  

4. **What do font-size, font-weight, and font-style do to HTML text elements?**  
    * Font-size: changes the size of the text according to the specified px, em, rem, or percentage set.
    * Font-weight: Sets how bold the text is. The most common values to use for bold are 'normal', or 'bold'.
    * Font-style: Used to turn italic text on or off.

5. **Describe two ways you could add spacing around the characters displayed in an h1 element.**  
Via 'letter-spacing' or 'word-spacing'.

## Links to resources used for these notes

* [Using Images in HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML)
* [Common Image Types](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types)
* [Choosing Image Formats](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Image_types#choosing_an_image_format)
* [Using Color in CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Colors/Applying_color)
* [Styling HTML Text Elements](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals)
