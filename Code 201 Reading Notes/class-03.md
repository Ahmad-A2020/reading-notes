##  Summarization From the Duckett HTML book:

### Chapter 3: “Lists” (pp.62-73)
There are various types of lists including the following:  
- Ordered Lists:  The ordered list is created with the `<ol>` element. Each item in the list is placed between an opening `<li>` tag and a closing `</li> `tag. 
- Unordered Lists: The unordered list is created with the `<ul>` element. Each item in the list is placed between an opening `<li>` tag and a closing `</li>` tag.
- Definition Lists: The definition list is created with the `<dl> `element and usually consists of a series of terms and
their definitions. Inside the `<dl>` element you will usually see pairs of `<dt> `and `<dd>` elements.`<dt> `: This is used to contain the term being defined (the definition term). `<dd>`:This is used to contain the definition.
- Nested Lists: You can put a second list inside  an `<li>` element to create a sublist or nested list.

### Chapter 13: “Boxes” (pp.300-329):
- By default a box is sized just big enough to hold its contents. To set your own dimensions for a box you can use the height and width properties.
- the **min-width property:** specifies the smallest size a box can be displayed at when the browser window is narrow, and the **max-width property:** indicates the maximum width a box can stretch to when the browser window is wide. - In the same way that you might want to limit the width of a box on a page, you may also want to limit the height of it. This is achieved using the min-height and max-height properties.
- The **overflow property:** tells the browser what to do if the content contained within a box is larger than the box itself. It can have one of two values: *hidden* This property simply hides any extra content that does not fit in
the box. *scroll* This property adds a scrollbar to the box so that users can scroll to see the missing content.
- The **border-width property:** is used to control the width of a border. The value of this property can either be given in pixels or using one of the following values: *thin, *medium*, or *thick*.
- You can control the style of a border using the **border-style property**. This property can take the following values:
*solid* a single solid line, *dotted* a series of square dots, *dashed* a series of short lines double two solid lines,  *groove* appears to be carved into the page, *ridge* appears to stick out from the page, *inset* appears embedded into
the page,*outset* looks like it is coming out of the screen, or *hidden / none* no border is shown.  
- **Border Color Property:** You can specify the color of a border using either RGB values,hex codes or CSS color names.
- The **border property** allows you to specify the width, style and color of a border in one property.
- The **padding property** allows you to specify how much space should appear between the content of an element and its
border.
- The **margin property** controls the gap between boxes. Its value is commonly given in pixels, although you may also use
percentages or ems.
- The **display property** allows you to turn an inline element into a block-level element or vice versa, and can also be used to hide an element from the page. The values this property can take are:*inline* This causes a block-level
element to act like an inline element. *block* This causes an inline element to act like a block-level element.
*inline-block* This causes a block-level element to flow like an inline element, while retaining other
features of a block-level element. *none*This hides an element from the page.
- The **visibility property** allows you to hide boxes from users but It leaves a space where the element would have been.
This property can take two values: *hidden* This hides the element. *visible* This shows the element.
- The **border-image property** applies an image to the border of any box. It takes a background image and slices it into nine. This property requires three pieces of information:
    - The URL of the image.
    - Where to slice the image.
    - What to do with the straight edges; the possible values are: *stretch*; stretches the image, *repeat*; repeats the image, and *round*; like repeat but if the tiles do not fit exactly, scales the tile image so they will pieces.

- The **box-shadow property** allows you to add a drop shadow around a box. It must use at least the first of these two
values as well as a color: *Horizontal offset*; Negative values position the shadow to the left of the box, *Vertical offset*; Negative values position the shadow to the top of the box,*Blur distance*; If omitted, the shadow is a solid
line like a border, and *Spread of shadow*; If used, a positive value will cause the shadow to expand in all directions, and a negative value will make it contract.
- **border-radius property** CSS3 introduces the ability to create rounded corners on any box, using a property called
border-radius. The value indicates the size of the radius in pixels.

## From the Duckett JS book:

### Review from Reading 02 - Chapter 2: “Basic JavaScript Instructions” (pp.70-73)
#### Array: 
An array is a special type of variable. It doesn't just store one value; it stores a list of values. in javasript, You can create an array and give it a name just like you would any other variable (using the var keyword followed by the name of the array). The values are assigned to the array inside a pair of square brackets, and each value is separated by a comma. take the following example: `colors= ['white', 'black', 'custom'];`
- Values in an array are accessed as if they are in a numbered list. It is important to know that the numbering of this list starts at zero (not one). Each item in an array is automatically given a number called an index. This can be used
to access specific items in the array. To retrieve the third item on the aformentioned above list, the array name is specified along with the index number in square brackets as following: `itemThree = col ors [ 2] ;` .
- You can change the value of an item an array by selecting it and assigning it a new value just as you would any other variable as fllowing: `colors[2] = 'beige ' ;`
 
### Chapter 4: “Decisions and Loops” from switch statements on (pp.162-182)
A switch statement starts with a variable called the switch value. Each case indicates a possible value for this variable and the code that should run if the variable matches that value.
##### if vs switch

IF ... ELSE
- There is no need to provide an el se
option. (You can just use an if
statement.)
- With a series of if statements, they are
all checked even if a match has been found
(so it performs more slowly than switch).
||
SWITCH
- You have a default option that is run if
none of the cases match.
- If a match is found, that code is run; then
the break statement stops the rest of
the switch statement running (providing
better performance than multiple i f
statements).
