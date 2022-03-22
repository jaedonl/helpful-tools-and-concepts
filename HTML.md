HTML
The HTML document type declaration, also known as DOCTYPE, is the first line of code required in every HTML or XHTML document. The DOCTYPE declaration is an instruction to the web browser about what version of HTML the page is written in. This ensures that the web page is parsed the same way by different web browsers.

1. How to serve a page with content in multiple languages?
- "lang" attribute
<html lang="en">
To change the language, just simply set the lang attribute. We can define it anywhere in the document, such as in the body, in the paragraph, in the heading, or in the span tag. But the best practice is to set the lang in the span tag.
<p> French " <span lang="fr"> Bonjour </span> " </p>


What are data- attributes good for?
- data-* attributes allow us to store extra information on standard, semantic HTML elements without other hacks such as non-standard attributes, or extra properties on DOM. 

2. What are the building blocks of HTML5?
Semantics — Allowing you to describe more precisely what your content is.
Connectivity — Allowing you to communicate with the server in new and innovative ways.
Offline and storage — Allowing webpages to store data on the client-side locally and operate offline more efficiently.
Multimedia — Making video and audio first-class citizens in the Open Web.
2D/3D graphics and effects — Allowing a much more diverse range of presentation options.
Performance and integration — Providing greater speed optimization and better usage of computer hardware.
Device access — Allowing for the usage of various input and output devices.
Styling — Letting authors write more sophisticated themes.

3. Describe the difference between a cookie, sessionStorage and localStorage.
cookie
Initiator — Client or server. Server can use Set-Cookieheader
Expiry — Manually set
Persistent across browser sessions —
Depends on whether expiration is set
Have domain associated — Yes
Sent to server with every HTTP request — Yes
Capacity (per domain) — 4kb
Accessibility — Any window

localStorage
Initiator — Client
Expiry — Forever
Persistent across browser sessions — Yes
Have domain associated — No
Sent to server with every HTTP request — No
Capacity (per domain) — 5MB
Accessibility — Any window

sessionStorage
Initiator — Client
Expiry — On tab close
Persistent across browser sessions — No
Have domain associated — No
Sent to server with every HTTP request — No
Capacity (per domain) — 5MB
Accessibility — Same tab

4. Describe the difference between <script>, <script async> and <script defer>.
script is HTML parsing is blocked, the script is fetched and executed immediately, HTML parsing resumes after the script is executed.
Async and defer are basically two boolean attributes for the <script> tag. Async allows the execution of scripts asynchronously as soon as they're downloaded. Defer allows execution only after the whole document has been parsed.

5. Why is it generally a good idea to position CSS <link>s between <head></head> and JS <script>s just before </body>? Do you know any exceptions?
- Putting stylesheet at the bottom of the document is that it prohibits progressive rendering in many browsers. Some browsers block rendering to avoid having to repaint elements of the page if their styles change.
- script's block HTML parsing while they are being downloaded and executed. Downloading the scripts at the bottom will allow the HTML to be parsed and displayed to the user first.
- exceiption for putting script at the top is when we have document.write() (but this is not a good way)

6. What is progressive rendering?
Progressive rendering is the name given to techniques used to improve performance of a webpage (in particular, improve perceived load time) to render content for display as quickly as possible.

Lazy loading of images — Images on the page are not loaded all at once. JavaScript will be used to load an image when the user scrolls into the part of the page that displays the image.

Prioritizing visible content (or above-the-fold rendering) — Include only the minimum CSS/content/scripts necessary for the amount of page that would be rendered in the users browser first to display as quickly as possible, you can then use deferred scripts or listen for the DOMContentLoaded/load event to load in other resources and content.

Async HTML fragments — Flushing parts of the HTML to the browser as the page is constructed on the back end. More details on the technique can be found here.

7. Why you would use a srcset attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.
- You would use the srcset attribute when you want to serve different images to users depending on their device display width - serve higher quality images to devices with retina display enhances the user experience while serving lower resolution images to low-end devices increase performance and decrease data wastage
<img srcset="small.jpg 500w, medium.jpg 1000w, large.jpg 2000w" src="..." alt=""/>

8. Have you used different HTML templating languages before?
- Liquid

9. What is the difference between canvas and svg?
An SVG image is drawn out using a series of statements that follow the XML schema — that means SVG images can be created and edited with any text editor, such as Notepad. There are several other advantages of using SVG over other image formats like JPEG, GIF, PNG, etc.

The HTML element is used to draw graphics on the fly, via scripting (usually JavaScript). The element is only a container for graphics. You must use a script to actually draw the graphics. Canvas has several methods for drawing paths, boxes, circles, text, and adding images.

<canvas id="newCanvas" width="100" height="100"></canvas>
<script>
    var c = document.getElementById('newCanvas');
    var ctx = c.getContext('2d');
    ctx.fillStyle = '#7cce2b';
    ctx.fillRect(0, 0, 100, 100);
</script>

10. What are empty elements in HTML ?
- element which can't have child element.
<area> <base> <br> <col> <embed> <hr> <img> <input> <link> <meta> <param> <source> <track> <wbr>