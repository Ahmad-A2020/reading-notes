## Chapter 10: Introducing CSS
Cascading Style Sheets is a style sheet language used for describing the presentation of a document written in a markup language such as HTML. CSS is a cornerstone technology of the World Wide Web, alongside HTML and JavaScript.
CSS works by associating rules with HTML elements. These rules govern how the content of specified elements should be displayed. A CSS rule contains two parts: a **selector** and a **declaration**. ***Selectors*** indicate which element the rule applies to. The same rule can apply to more than one element if you separate the element names with commas. ***Declarations*** indicate how the elements referred to in the selector should be styled. Declarations are split into two
parts (a property and a value), and are separated by a colon.
**Example:**
h1(This is **selector**) {
  color: white;
  text-align: center;
} (The remaining is the **declaration** )

There are two method to use the CSS in HTML file as follows: 
- Using External CSS: The CSS code invoke inside the HTML file usine <**link**>.The <**link**> element can be used
in an HTML document to tell the browser where to find the CSS file used to style the page. It is an empty element (meaning it does not need a closing tag), and it lives inside the <**head**> element. It should use three attributes:
***href**; This specifies the path to the CSS file (which is often placed in a folder called css or styles). 
***type***;This attribute specifies the type of document being linked to. The value should be text/css.
***rel** This specifies the relationship between the HTML page and the file it is linked to. The value should be stylesheet when linking to a CSS file.
- Using Internal CSS: The CSS script add within <**style**> element, on which You can also include CSS rules
within an HTML page by placing them inside a <**style**> element, which usually sits inside the <**head**> element of the page. The <**style**> element should use the type attribute to indicate that the styles are specified in CSS. The value should be text/ css.

## Chapter 11 : Color
The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways as following :
- rgba values: These express colors in terms of how much red, green and blue are used to make it up. 
For example: rgb(100,100,90). a valus is for opacity property which allows you to specify the opacity of an element
and any of its child elements.The value is a number between 0.0 and 1.0
- hex codes: These are six-digit codes that represent the amount of red, green and blue in a color, preceded by a pound or hash # sign. 
For example: #ee3e80
- color names: There are 147 predefined color names that are recognized by browsers.
For example: DarkCyan.
-  has also introduced
another way to specify colors
-  HSLA: it is an additional way that introduced by CSS3, which stands for hue, saturation, lightness, and Alpha values.**Hue**; Hue is the colloquial idea of color. In HSL colors, hue is often represented as a color circle where the angle represents the color, although it may also be shown as a slider with values from 0 to 360. ***Saturation**;Saturation is the amount of gray in a color. Saturation is represented as a percentage. 100% is full saturation and 0% is a shade of gray.**lightness** Lightness is the amount of white (lightness) or black (darkness) in a color. Lightness is represented as a percentage. 0% lightness is black, 100% lightness is white, and 50% lightness is normal. Lightness is sometimes referred to as luminosity. **Alpha** This is expressed as a number between 0 and 1.0. For example, 0.5 represents
50% transparency, and 0.75 represents 75% transparency.


