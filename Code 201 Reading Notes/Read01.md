## Duckett HTML book:

### Introduction (pp.2-11):
- There are three different ways in which people access the web: **web browser** such as Chrome, and Opera; **web server** which hosts the website; **devices** including desktop computers, laptops, tablets, and mobile phones.
- How the Web works: 
   - The browser goes to the DNS(Domain Name System) server, and finds the real address of the server that the website lives on .
   - The browser sends an HTTP request message to the server, asking it to send a copy of the website to the client (you go to the shop and order your goods). This message, and all other data sent between the client and the server, is sent across your internet connection using TCP/IP.
   - If the server approves the client's request, the server sends the client a "200 OK" message, which means "Of course you can look at that website! Here it is", and then starts sending the website's files to the browser as a series of small chunks called data packets.

### HTML Chapter 1: “Structure” (pp.12-39)
The web page is structured using the HTML language; HTML utilize a group of elements to describe the structure of the page. Each element has an opening tag and a closing tag. Tags act like containers. They tell you something about the information that lies between their opening and closing tags. The openiing tag may includes Attributes which aim at provideing additional information about the contents of an element. It is made up of two parts: a name and a value,separated by an equals sign. Below is an example of a paragraph element that used at the HTML: 

`<p lang="en-us">Paragraph in English</p>`

### HTML Chapter 8: “Extra Markup” (p.176-199): 

here is some of the HTML elements: 
- `<DOCTYPES html>`: Because there have been several versions of HTML, each web page should begin with a DOCTYPE declaration to tell a browser which version of HTML the page is using
- `<!-- -->`: If you want to add a comment to your code that will not be visible in the user's browser, you
can add the text between these characters.
- **ID Attribute:** Every HTML element can carry the id attribute. It is used to uniquely identify that element from other elements on the page. Its value should start with a letter or an underscore (not a number or any other character). It is important that no two elements on the same page have the same value for their id attributes (otherwise the value is no longer unique).
 - **Class Attribute:** Every HTML element can also carry a class attribute. Sometimes, rather than uniquely identifying one element within a document, you will want a 
way to identify several elements as being different from the other elements on the page.
 - `<iframe>` An iframe is like a little window that has been cut into your page — and in that window you can see another page. The term iframe is an abbreviation of inline frame. There are a few attributes that used within this element: *scr*is for specifies the URL of the page to show in the frame, *height* is for determine the height of the frame in pixels, *width* is to specifies the width attribute the iframe in pixels.
 - `<meta>` This element lives inside the `<head>` element and contains information about that web page.It uses attributes to carry the information. The most common attributes are the name and content attributes, which tend to be used together.
 - `<div>` It is an important way to group together related elements. 
 - `<span>` it is acts like an inline equivalent of the `<div>` element. It is used to either: Contain a section of text
where there is no other suitable element to differentiate it from its surrounding text or Contain a number of inline elements.

### HTML Chapter 17: “HTML5 Layout” (pp.428-451):

HTML5 introduces a new set of elements that allow you to divide up the parts of a page. The names of these elements indicate the kind of content you will find in them. Following you will find some of them: 
- `<header> & <footer>`: They can be used for: The main header or footer that appears at the top or bottom of every page on the site. Also, for A header or footer for an individual article or section within the page.
- `<nav>`: The element is used to contain the major navigational blocks on the site such as the primary site navigation.
- `<article>`:It is acts as a container for any section of a page that could stand alone and potentially be syndicated. This could be an individual article or blog entry, a comment or forum post, or any other independent piece of content.
- `<aside>`: The `<aside>` element has two purposes, depending on whether it is inside an `<article>` element or not. When the <aside> element is used inside an article element, it should contain information that is related to the article but not essential to its overall meaning. For example, a pullquote or glossary might be considered as an aside to the article it relates to. When the `<aside>` element is used outside of an `<article>` element, it acts as a container for content that is related to the entire page. For example, it might contain links to other sections of the site, a list of recent posts, a search box, or recent tweets by the author.
- `<section>`: It groups related content together, and typically each section would have its own heading.
- `<figure>`: It can be used to contain any content that is referenced from the main flow of an article  such as images.

### HTML Chapter 18: “Process & Design” (pp.452-475)
This chapter aims at providing the web-developer of the process required for creating new web site: 
-  **First Step:** *Determine the the web site audiance that the site target*; At the level of the individual we may intrest in : users age range, the users' countries, level of education for the users,  users' income, users' occupation,and no of the working hours. For companies, the major points that we may intrest to know when creat the web site is: the size of company, position of people in the company who visit your site, amount of budget that the company control. 
- **Second Step:** *Determine the reason that the people may visit the created website*; like looking for time
sensitive information, such as the latest news or updates on a particular topic.
- **Third Step:** Determine What visitors are trying to achieve; what means is the key tasks and motivations.
- **Forth Step:** *Determine Information web site that visitors need*; By this you may want to offer additional
supporting information that you think they might find helpful.
- **Fifth Step:** *Determine the method that the users will visit your site;* Some sites benefit from being updated more frequently than others. Some information (such as news) may be constantly changing, while other content remains relatively static. 
- **Sixth Step:** *create of the site map;* Now that you know what needs to appear on your site, you can start to organize the information into sections or pages.

After that you can start to make sketch for your web page, which called wireframe.
 ### **wireframe:**
 wireframe is a simple sketch of the key information that needs to go on each page of a site. It shows the hierarchy of the information and how much space it might require. By creating a wireframe you can
ensure that all of the information that needs to be on a page is included.It should focus on what
information needs to be on each page and create a visual hierarchy to indicate the most important parts of each page.
### **Visual hierarchy**
refers to the order in which your eyes perceive what they see. It is created by adding visual contrast between the items being displayed. Items with higher contrast are recognized and processed first.Most web users do not read entire pages. Rather, they skim to find information. You can use contrast to create a visual hierarchy that gets across your key message and helps users find what they are looking for. You can differentiate between pieces of information using size, color, and style.
You can use grouping and similarity to help simplify
### **grouping and Similarity:** 
When making sense of a design, we tend to organize visual elements into groups. Grouping related pieces of information together can make a design easier to comprehend. There are many ways this can be achieved including: Proximity, Closure, Continuance, White Space, color, Borders. 

## From the Duckett JS book:

### Introduction:
Over this part the writer mention for the reader how to use the book, the main content of the book, what each chapter at the book includes, and revision for HTML and CSS languages. After that, he moved to give the reader brieve introduction about this language for the biggener. Following points higlight main aspects in this part of the book. 
#### The major features that the javascript add to the web page is that it makes the webpage more interactive including:  
- ACCESS CONTENT: You can use JavaScript to select any element, attribute, or text from an HTML page.
- MODIFY CONTENT: You can use JavaScript to add elements, attributes, and text to the page, or remove them
- PROGRAM RULES: You can specify a set of steps for the browser to follow (like a recipe), which allows it to access or change the content of a page
- REACT TO EVENTS: You can specify that a script should run when a specific event has occurred.
### JS Chapter 1: “The ABC of Programming” (pp.11-52)
#### **script:**
 it is a series of instructions that a computer can follow to achieve a goal. You could compare scripts to any of the following: RECIPES, HANDBOOKS, or MANUALS. 
- **How to Write A script:** To write a script, you need to first state your goal and then list the tasks that need to be completed in order to achieve it.then, you have to design a script by splitting the goal out into a series of tasks that are going to be involved in solving this puzzle, which cane be represented using a flowchart. Finally, you can start coding each step written in a programming language that the computer 
understands such as javascript.
- **how a browser sees a web page:**
    - receive a page as html code: Each page on a website can be seen as a separate document . So, the web consists of  many sites, each made up of one or more documents.
    - create a model of the page and store it in memory: 
    - use a rendering engine to show the page on screen:If there is no CSS, the rendering engine will apply default styles to HTML elements, but When the browser receives CSS rules, the rendering engine processes them and applies each rule to its corresponding elements.
    - When you use JavaScript in the browser, there is a part of the browser that is called an interpreter The interpreter takes your instructions (in JavaScript) and translates them into instructions the browser can use to achieve the tasks you want it to perform.

developers usually use three languages to create web pages: HTML, CSS, and JavaScript. They useually keep the three languages in separate files,with the HTML page linking to CSS and JavaScript files. Each language forms a separate
layer with a different purpose as following. These three layers form the basis of a popular approach to building web pages called progressive enhancement.
- CONTENT LAYER(. html files): This is where the content of the page lives. The HTML gives the page structure and adds semantics.
- PRESENTATION LAYER(.css files):The CSS enhances the HTML page with rules that state how the HTML content is presented.
- BEHAVIOR LAYER(.js files): This is where we can change how the page behaves, adding interactivity. the javascript file is linked to HTML page by `<script>` element to tell the browser to load the JavaScript file. Its s reattribute tells people where the JavaScript file is stored.