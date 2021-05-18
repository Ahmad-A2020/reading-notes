**Cookies:** are messages that web servers pass to your web browser when you visit Internet sites. Your browser stores each message in a small file, called cookie.txt. When you request another page from the server, your browser sends the cookie back to the server. These files typically contain information about your visit to the web page, as well as any information you've volunteered, such as your name and interests.
#### HTML5 STORAGE
Definiation : it’s a way for web pages to store named key/value pairs locally, within the client web browser.
proarities: 
-The data stored at the HTML storage is persists even after you navigate away from the web site, close your browser tab, exit your browser, or what have you. 
- The data stored at the HTML storage is never transmitted to the remote web server (unless you go out of your way to send it manually). Unlike all previous attempts at providing persistent local storage, it is implemented natively in web browsers, so it is available even when third-party browser plugins are not.
- To access HTML5 Storage, this is done through the localStorage object on the global window object using the getItem() and setItem() methods. There are also methods for removing the value for a given named key such as removeItem(). 