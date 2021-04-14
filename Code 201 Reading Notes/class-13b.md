### Transforms
- No one worried that the rest of the team was judging them
**Definition:**The transform property applies a 2D or 3D transformation to an element. This property allows you to rotate, scale, move, skew, etc., elements.
- the transform property includes multiple vendor prefixes to gain the best support across all browsers including: -webkit-transform, -moz-transform, -o-transform, and tansform.
- for the two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes.The transform property accepts a handful of different values including: the *rotate value* provides the ability to rotate an element from 0 to 360 degrees suc as   `transform: rotate(20deg)`; the *scale value* within the transform property allows you to change the appeared size of an element such as `transform: scale(.75)`; the *translate value* works a bit like that of relative positioning, pushing and pulling an element in different directions without interrupting the normal flow of the document such as `transform: translateX(-10px)`; and *transform value* ,on which skew is used to distort elements on the horizontal axis, vertical axis, or both such as   `transform: skewX(5deg)` in x-axis, ` transform: skewY(-20deg)` in Y-axis, and `transform: skew(5deg, -20deg)` in the two axies. 
- To combine transforms, list the transform values within the transform property one after the other without the use of commas such as `transform: rotate(25deg) scale(.75)`.
- For the three-dimensional transforms work on both the x and y axes, as well as the z axis. These three-dimensional transforms help define not only the length and width of an element, but also the depth. The 3D transform property accepts a handful of different values including: *3D Rotate* to rotate an object either clockwise or counterclockwise on a flat plane such as `rotateX(45deg)` to rotate the object around the x axis, `rotateY(45deg)` to rotate the object around the  axis,  and `rotateZ(45deg)` to rotate the object around the z axis; *scaleZ* three-dimensional transform elements may be scaled on the z axis; and *translateZ* value that used for translated element on the z axis.

### Transitions & Animations
- Transitions provide a change from one state to another.for a transition to take place, an element must have a change in state, and different styles must be identified for each state.The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target pseudo-classes.
- There are four transition related properties in total, including *transition-property*, *transition-duration*, *transition-timing-function*, and *transition-delay*.
- The following CSS code is create box that will change its background color over the course of 1 second in a linear fashion.
   - .box {
    background: #2db34a;
    transition-property: background;
    transition-duration: 1s;
    transition-timing-function: linear;
    }
    .box:hover {
    background: #ff7b29;
    }

- The duration in which a transition takes place is set using the transition-duration property. The value of this    property can be set using general timing values, including seconds (s) and milliseconds (ms).
- The transition-timing-function property is used to set the speed in which a transition will move.
- On top of declaring the transition property, duration, and timing function, you can also set a delay with the transition-delay property. 


