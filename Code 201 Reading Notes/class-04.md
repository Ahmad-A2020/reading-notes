## Summarized From the Duckett HTML book:

### Chapter 4: Ch.4 “Links” (pp.74-93)
The element use in HTML to write line is `<a>` element such as `<a href="http://www.imdb.com">IMDB</a>`which has an attribute called href. The value of the
href attribute is the page that you want people to go to when they click on the link.
There are differtent type of links including :
- Links from one website to another:in this case, the value of the href attribute will be the full web address for the site **(absolute URL)**.
-  Links from one page to another on the same website: in such case, you need only You to use a shorthand known as a **relative URL**.
- Links from one part of a web page to another part of the same page: to da that, you need two steps: 
     - Identify the points in the page
     that the link will go to. You do
     this using the id attribute.
     - use the `<a>` element again, but the value of the href attribute starts with the # symbol, followed by the value of the id attribute of the element you want to link to.
   
-  Links that open in a new browser window: for this purpose use the target attribute on the opening `<a>` tag. The value of this attribute should be _blank.
-  Links that start up your email program and address a new email to someone: in this case  the value of the href attribute starts with mailto: and is followed by the email address you want the
email to be sent to.


### Chapter 15: “Layout” (pp.358-404)
- **containing or parent element**: If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.
- It is common to group a number of elements together inside a `<div>`.

- CSS has the following positioning  schemes that allow you to control the layout of a page, on which you can specify using the position
property: 
   - normal flow positioning (position:static): This the default browser window scheme. 
   -  relative positioning (position:relative): moves an element in relation to where it would have been in normal flow. 
   
   - absolute positioning (position:absolute): in this position the box is taken out of normal flow and no longer affects the position of other elements on the page. 
   - Fixed Positioning (position:fixed): It positions the element in relation to the browser window.