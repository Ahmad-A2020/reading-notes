## The following content are summarized From the Duckett HTML book:

### Chapter 5: “Images” (pp.94-125)
- **`<img> `element:**  to add an image into the page you need to use an `<img>`
element. This image element must carry the following two attributes:
   -  *src:* This tells the browser where it can find the image file.
   - *alt:* this provides a text description of the image which describes the image if you cannot see it.
   - *title:* You can also use the title attribute with the `<img>` element to provide additional information about the image.
The `<img>` element may use two other attributes that specify its size: 
   - *height*: This specifies the height of the image in pixels.
   - *width*: This specifies the width of the image in pixels. 
determine the plce of the photo: the place of the photo identify through determine where you add in the code. for example, if you added it before the paragraph, then The paragraph starts on a new line after the image. Moreover, htmal use the **align** attribute to align picture horizentally and vertic ally.
The align attribute can take these horizontal values: *left* This aligns the image to the left (allowing text to flow around its right-hand side). *right*
This aligns the image to the right
(allowing text to flow around its
left-hand side). for the vertical alignment, there are three values that the
align attribute can take control how the image should align vertically with the text that surrounds it: *top* this aligns the first line of the surrounding text with the top of the image, *middle*;
this aligns the first line of the
surrounding text with the middle
of the image,*bottom*; this aligns the first line of the surrounding text with the bottom of the image.

### Chapter 11: “Color” (pp.246-263)

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

### Chapter 12: “Text” (pp.264-299)

**Specifying Typefaces**
- The *font-family property* allows you to specify the typeface that should be used for any text inside the element(s) to which a CSS rule applies.
- The *font-size property* enables you to specify a size for the font. There are several ways to specify the size of a font. The most common are: *pixels*;Pixels are commonly used because they allow web
designers very precise control over how much space their text takes up. The number of pixels is followed by the letters px, and *percentage*; the default size of text in browsers is 16px. 
- The **font-weight property**
allows you to create bold text.
There are two values that this property commonly takes:*normal*;this causes text to appear at a normal weight, and *bold*; this causes text to appear bold.
- If you want to create italic text,
you can use the **font-style property**. There are three values this property can take: *normal*; this causes text to appear in a normal style (as opposed to italic or oblique), *italic*;this causes text to appear italic, and *oblique*;this causes text to appear oblique.
- The **text-transform property**
is used to change the case of text giving it one of the following values: *uppercase*; this causes the text to appear uppercase, *lowercase*; this causes the text to appear lowercase, and 
*capitalize*;this causes the first letter of each word to appear capitalized.
- The **text-decoration property** allows you to specify the following values: *none*; this removes any decoration
already applied to the text, *underline*; this adds a line underneath the text, *overline*; this adds a line over the top of the text, *line-through*; this adds a line through words, and *blink*;this animates the text to make it flash on and off. 
- the **line-height property** sets the height of an entire line of text.
- **word-spacing property**: you can control the gap between words using the word-spacing property.
- **letter-spacing property**: you can control the gap between letter within the word using the letter-spacing property.

## JPEG vs PNG vs GIF: 

There are alot of photos formate exist, but JPEG, PNG and GIF formats together comprise of more than 95% of all images loaded on websites. Selecting any one of these formate depends on the what is natural of the picture itself as following: 
- JPEG format: for all images that contain a natural scene or photograph where variation in colour and intensity is smooth. 
- PNG format: Use it for any image that needs transparency or for images with text & objects with sharp contrast edges like logos. 
- GIF format: Use it for images that contain animations.
To reduce the size of data and ensure faster transmission, the photos usually commpressed. There are two type of compression:*lossless*; in this type, it is possible to reconstruct the original image from the compressed image because there is no information loss during compression such as **PNG** and **GIF** formates, and the second type of compression photos is *lossy*; on which the data loss during the compression like. An example on the later one is   
**JPEG** formate.

**Transparency:** it is indicate that the is invisible. for JPEG images don’t support transparency and are hence not usable for such cases, while PNG images , and GIF images are supporting the transparency. 
<!-- the first one allows partial transparency, which  makes the edges blend smoothly into the background, whereas the later one  -->
**Colours:** JPEG images can support around 16 million colours. for PNG images mainly have two modes — PNG8 and PNG24. PNG8 can support upto 256 colours whereas PNG24 can handle upto 16 million colours like a JPEG image. finally, GIF images are limited to 256 colours.
**Animation:** of the three aformentioned formates only GIF supports animation.
Finally `ImageKit.io` is a cloud-based image optimisation and transformation product that can automatically deliver images in the most suitable format.

Note: Resourses of this summarization are from this blog (https://redirect.is/3116c5p). 
