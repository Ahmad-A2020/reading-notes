### [lab](https://github.com/Ahmad-A2020/cookie-stand):
![lab9](/Code 201 Reading Notes/screenShot/lab9-1.PNG)
![lab9](/Code 201 Reading Notes/screenShot/lab9-2.PNG)

### Summarized from the Duckett HTML book:

#### Chapter 7: “Forms” (p.144-175)

There are several types of form controls that you can use to collect information rom visitors to your site: 
- ADDING TEXT: This includes; Text input (single-line),Password input, and Text area (multi-line). 
- Making Choices:This includes;Radio buttons, Checkboxes, and Drop-down boxes. 
- Submitting Forms:This includes; Submit buttons, and Image buttons. 
- Uploading Files:

##### The way the form is working: 
- ist Step: A user fills in a form and then presses a button to submit the information to the server.
- 2nd step: The name of each form control is sent to the server along with the value the user enters or selects.
- 3rd step: The server processes the information using a programming language such as PHP, C#, VB.net, or Java. It may also store the information in a
database. 
- 4th step: The server creates a new page to send back to the browser based on the
information received.
##### Form Structure:
To create form in HTML you have to use `<form>` element, on which the form controls live inside a `<form>` element. This element should always carry the *action attribute* and will usually have *a method* and *id* attribute too. For the **action** method; it carry the value of the URL for the page on the server that will receive the information in the form when it is submitted. Moving to the 
**method** attribute; is to select the way that the form will be sent using one of
two methods: get or post.With the *get method*, the values from the form are added to the end of the URL specified in the action attribute. This way is recommended in short forms, and when you are just retrieving data from the web server.With the *post method* the values are sent in what are known as HTTP headers. As a rule of thumb you should use the post method if your form allows users to upload a file,  is very long, contains sensitive data, or adds information to, or deletes information from, a database. inside the `<form>` element, the following elements may use according to the website needs: 
- `<input>`: it is used to create several different form controls. The value of the type attribute determines what kind
of input they will be creating. this element includes the following attributes: *type*="text"; When the type attribute has a value of text, it creates a singleline text input, *name*; it holds the name of the cell that the user will fill in to, *maxlength*;you can use the maxlength attribute to limit the number of characters a user may enter into the text field.
- `<textarea>` element: it is used to create a mutli-line text input.
- Radio Button: Radio buttons allow users to pick just one of a number of options.To create this tool we use the `<input>` elment , on which the attribute is assigned to *type="radio"*. For *name* attribute, the name attribute is sent to the server with the value of the option the user selects. another attribute is *value*; the value attribute indicates
the value that is sent to the server for the selected option. Finally, the *checked* attribute can be used to indicate which value (if any) should be selected when the page loads.
- Checkboxes:  allow users to select (and unselect) one or more options in answer to a question. To create this tool we use the `<input>` elment , on which the attribute is assigned to *type="checkbox". the remaining three attribute same as the previous point. 
- drop down list box:
- Multiple Se lec t Box:
- File Input Box:
- Submit Button:
  
#### Chapter 14: “Lists, Tables & Forms” (pp.330-357)
###### List Properties:
using the CSS you can add some proparities to the list, here are some of theses: 
- The *list-style-type* property: allows you to control the shape or style of a bullet point (also known as a marker).
- *list-style-image*: you can specify an image to act as a bullet point using the list-style-image property.
- *list-style-position*: it ndicates whether the marker should appear on the inside or the outside of the box containing  the main points.
- *list-style*: it allows you to express the markers' style, image and position properties in any order.

###### Table Properties:
-width: to set the width of the table
- padding: to set the space between the border of each table cell and its content
- text-transform: to convert the content of the table headers to uppercase
- letter-spacing, font-size to add additional styling to the content of the table headers - border-top, border-bottom to set borders above and below the table headers
- text-align to align the writing to the left of some table cells and to the right of the others
- background-color to change the background color of the alternating table rows - :hover to highlight a table row when a user's mouse goes over it

### Summarized from the Duckett JS book:

####  Chapter 6: “Events” (pp.243-292):
Below is some of the event: 
- load: Web page has finished loading
- unload: Web page is unloading (usually because a new page was requested)
- error: Browser encounters a JavaScript error or an asset doesn't exist
- resize: Browser window has been resized
- scroll: User has scrolled up or down the page