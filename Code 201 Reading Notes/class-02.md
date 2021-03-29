##  Summarizing From the Duckett HTML book:

### Chapter 2: “Text” (pp.40-61)

- `<h1> `,`<h2>`, `<h3>,` `<h4>`, `<h5>`, `<h6>` elements: HTML has six "levels" of headings: `<h1>` is used for main  eadings `<h2>` is used for subheadings If there are further sections under the subheadings then the `<h3>` element is used, and so on.
- `<p>` element: To create a paragraph, surround the words that make up the paragraph with an opening `<p> `tag and closing `</p>` tag. 
- `<b>` element : By enclosing words in the tags `<b>` and `</b>` we can make characters appear bold.
- `<i>` element: By enclosing words in the tags `<i>` and `</i>` we can make characters appear italic.
- `<sup>` element: The `<sup>` element is used to contain characters that should be superscript such as the suffixes of dates or  mathematical concepts like raising a number to a power such as 22.
- `<sub>` element:  The `<sub>` element is used to contain characters that should  be subscript. It is commonly
used with foot notes or chemical formulas such as H20.
- `<br />` element: if you wanted to add a line break inside the middle of a paragraph you can use the line break tag `<br />`.
- `<hr />` element: you can add a horizontal rule between sections using the `<hr />` tag.
- `<strong>` element: The use of the `<strong>` element indicates that its content has strong importance. By default, browsers will show the contents of a `<strong>` element in bold.
- `<em>` element: The `<em>` element indicates emphasis that subtly changes the meaning of a sentence. By default browsers will show the contents of an `<em>` element in italic.
- `<blockquote>` element:  The `<blockquote>` element is used for longer quotes that take up an entire paragraph.
- `<q>` element: this is alos use for quotes, but this is for shorter quotes that sit within a paragraph.

 
### Chapter 10: Ch.10 “Introducing CSS” (pp.226-245)
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
## Summarizing from the Duckett JS book:

### Chapter 2: “Basic JavaScript Instructions” (pp.53-84)

- A script is a series of instructions that a computer can follow one-by-one. Each individual instruction or step is known as a **statement.**
- Some statements are surrounded by curly braces; these are known as **code blocks**. The closing curly brace is not followed by a semicolon.
- javascript allow you to write comments to explain what your code does using two methods: 
   - To write a comment that stretches over more than one line, you use a **multi-line comment**, starting with
    the /* characters and ending with the * / characters.
    - In a **single-lin**e** comment, anything that follows the two forward slash characters I/ on that line will not be processed by the JavaScript interpreter.
- **variables:** A script will have to temporarily store the bits of information it needs to do its job. It can store this data in variables. Before use variable, you need to declare them using var like `var quality`. following you can assign value in the variable live   `quality=5`.
-  There are various data type in javascripts including: numbers, strings, and true or false values known as
Booleans.The numeric data type handles numbers, and The strings data type consists of letters and other characters.
- if you want to use a double or single quote mark within a string. Two techniques could be used: 
    - **escaping** the quotation characters. This is done by using a backwards slash (or "backslash") before any type of
      quote mark that appears within a string.
    - if you just want to use double quotes in the string, you could surround the entire string in single quotes, while If you  just want to use single quotes in the string, you could surround the string in double quotes.
#### Array: 
An array is a special type of variable. It doesn't just store one value; it stores a list of values. in javasript, You can create an array and give it a name just like you would any other variable (using the var keyword followed by the name of the array). The values are assigned to the array inside a pair of square brackets, and each value is separated by a comma. take the following example: `colors= ['white', 'black', 'custom'];`
- Values in an array are accessed as if they are in a numbered list. It is important to know that the numbering of this list starts at zero (not one). Each item in an array is automatically given a number called an index. This can be used
to access specific items in the array. To retrieve the third item on the aformentioned above list, the array name is specified along with the index number in square brackets as following: `itemThree = col ors [ 2] ;` .
- You can change the value of an item an array by selecting it and assigning it a new value just as you would any other variable as fllowing: `colors[2] = 'beige ' ;`
#### Expressions + Operators: 

An expression: evaluates into (results in) a single value. Broadly speaking there are two types of expressions:
- Expressions that just assign a value to a variable.
- expressions that use two or more values to return a single value.
Operators: Operators are symbolic characters that specify the action to be performed on their associated operands. Each operand consists of one or more expressions or expression atoms. There are vatious type of the operators as follows: 
- Assignment operators : Assign a value to a variable.
- Arithmetic operators: Perform basic math; JavaScript contains the following mathematical operators, which you can use with numbers: addition + adds one value to another, - subtraction subtracts one value from another, division i divides two values, multiplication * multiplies two values using an asterisk, and modulus % Divides two values and returns the remainder
- String operators: There is just one string operator: the+ symbol.It is used to join the strings on either side of it.
- Comparison operators: Compare two values and return true or fa 1 se
- Logical operators: Combine expressions and return true or false    

### Chapter 4: “Decisions and Loops” only up to the section on switch statements (pp.145-162)

- **Comparison operators:** It is the operators that compare values and return true or false. The operators include: >(greater than), <(less than), >= (greater than or equal), <= (less than or equal to), === (strict equal to ),== (is equal to),!= (is not equal to), and !== (strict not equal to ).
- **Logical Operator:** It is a symbol or word used to connect two or more expressions such that the value of the compound expression produced depends only on that of the original expressions and on the meaning of the operator. Common logical operators include AND(&&), OR(\|\|), and NOT(!).logical operators are typically used with Boolean (logical) values. When it is, it returns a Boolean value.Starting with AND (&&), The logical  ( && ) operator (logical conjunction) for a set of operands is true if and only if all of its operands are true. moving to The logical OR (\|\|) operator (logical disjunction) for a set of operands is true if and only if one or more of its operands is true. Finally, The logical NOT (!) operator (logical complement, negation) takes truth to falsity and vice versa.