#### [lab](https://github.com/Ahmad-A2020/cookie-stand):
![lab6](/Code 201 Reading Notes/screenShot/lab6-1.PNG)
![lab6](/Code 201 Reading Notes/screenShot/lab6-2.PNG)
![lab6](/Code 201 Reading Notes/screenShot/lab6-3.PNG)
![lab6](/Code 201 Reading Notes/screenShot/lab6-4.PNG)
![lab6](/Code 201 Reading Notes/screenShot/lab6-5.PNG)
![lab6](/Code 201 Reading Notes/screenShot/lab6-6.PNG)
![lab6](/Code 201 Reading Notes/screenShot/lab6-7.PNG)

## The following chapters are summarized From the Duckett JS book

### Chapter 3: “Object Literals” (pp.100-105).

**Object:**is a collection of properties, and a property is an association between a name (or key) and a value. A property's value can be a function, in which case the property is known as a method.

- To access a property of the object, use name of the object, followed by a dot and then the name of the property or method that you want, or you can use the object name followed by the method name.

### Chapter 5: “Document Object Model” (pp.183-242).
**Defination:** Document Object Model (DOM) is a platform and language-neutral interface that allows programs and scripts to dynamically access and update the content, structure, and style of a document.
The Document Object Model (DOM) is a programming interface for HTML and XML documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects. That way, programming languages can connect to the page.
#### Step 1: Access the Elements: 
The DOM  defines methods and properties to access and update each object in this model, which in turn updates
what the user sees in the browser. Here is an overview of the methods and properties that access elements:
   - **get El ementByid ()**: this method has one parameter;the value of the id attribute on the element you want to select. This value is placed inside quote marks because it is a string.
   - **querySelector()**: uses a CSS selector, and returns the first matching element.
   - **getElementsByClassName()**: selects all elements that have a specific value for their class attribute.
   - **getElementsByTagName()**: Selects all elements that have the specified tag name.
   - **querySelectorAll()**: uses a CSS selector to select all matching elements.
   - **parentNode**: selects the parent of the current element node 
   - **previousSibling / nextSibling**: selects the previous or next sibling from the DOM tree.
   - **firstChild / lastChild**: select the first or last child of the current element.
#### Step 2:  Get/Update Element Content:
After reaching the node refereance, you can made update and change the value of the node, following is some properity that you may use: 
- textContent: sets or returns the text content of the specified node, and all its descendants.
- nodeValue: the nodeValue property sets or returns the node value of the specified node.
- innerHTML: using the innerHTML property, you can access and amend the contents of an element, including any child elements.
-  DOM manipulation: it  offers another technique to add new content to a page; It involves three steps:
    - You start by creating a new element node using the createElement() method; This element node is stored in a variable.
    - give it content using createTextNode(), which creates a new new text node. Again, the node is stored in a variable. It can be added to the element node using the appendChild () method.
    - Now text that you have your element new text node (optionally with some content in a text node) you can add added to DOM tree using the the appendChild()  method.
- DOM manipulation can be used to remove  elements from the DOM tree.
    - You start by selecting the element that is going to be removed and store that element node in a variable.
    - Next, you find the parent element that contains the element you want to remove and store that element node in a variable.
    - The removeChi ld() method is used on the containing element that you selected in step 2. The removeChi ld() method takes one parameter: the reference to the element that you no longer want.


