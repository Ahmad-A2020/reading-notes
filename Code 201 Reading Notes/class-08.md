### Summarized from From the Duckett HTML book:

#### Ch. 15, “Layout”:

- **containing or parent element**: If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.
- It is common to group a number of elements together inside a `<div>`.

- CSS has the following positioning  schemes that allow you to control the layout of a page, on which you can specify using the position property : 
   - normal flow positioning (position:static): This the default browser window scheme. In normal flow, each block-level element sits on top of the next one.
   -  relative positioning (position:relative): moves an element in relation to where it would have been in normal flow. 
   
   - absolute positioning (position:absolute): in this position the box is taken out of normal flow and no longer affects the position of other elements on the page. 
   - Fixed Positioning (position:fixed): It positions the element in relation to the browser window.
-**z-index**: When you use relative, fixed, or absolute positioning, boxes can overlap. If boxes do overlap, the elements that appear later in the HTML code sit on top of those that are earlier in the page. If you want to control which element sits on top, you can use the z-index property. Its value is a number, and the higher the number the closer that element is to the front.
- The float **property** allows you to take an element in normal flow and place it as far to the left or right of the containing element as possible.
- **Screen Resolution**: Resolution refers to the number of dots a screen shows per inch. 
