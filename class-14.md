# CSS Further
  * Transforms - comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.
    * The transform property accepts a handful of different values. The rotate value provides the ability to rotate an element from 0 to 360 degrees. Using a positive value will rotate an element clockwise, and using a negative value will rotate the element counterclockwise. The default point of rotation is the center of the element, 50% 50%, both horizontally and vertically
  * 2d scale - using the scale value within the transform property allows you to change the appeared size of an element.  It is possible to scale only the height or width of an element using the scaleX and scaleY values.  
  * 2D Translate - works a bit like that of relative positioning, pushing and pulling an element in different directions without interrrupting the normal flow of the document.  
  * 2D Skew - is used to distort elements on the horizontal axis, vertical axis, or both.  
  * Combining Transforms - it is common for multiple transorms to be used at once, rotating and scaling the size of an element at the same time. 
  * Transform origin - the transform origin is the dead center of an element.  It can only accept two values.  
  * Perspective - in order for three-dimensional transforms to work the elements need a perspective from which to transform.  The perspective for each element can be thought of as a vanishing point.  
  * Perspective Depth value - can be set as non or a length measurement.  The none value turns off any perspective, while the length value will set the depth of the perpective. 
  * Perspective origin - As with setting a transform-origin you can also set a perspective-origin. The same values used for the transform-origin property may also be used with the perspective-origin property, and maintain the same relationship to the element.
  * 3d Rotate - With three-dimensional transforms we can rotate an element around any axes. To do so, we use three new transform values, including rotateX, rotateY, and rotateZ. Using the rotateX value allows you to rotate an element around the x axis, as if it were being bent in half horizontally. Using the rotateY value allows you to rotate an element around the y axis, as if it were being bent in half vertically. Lastly, using the rotateZ value allows an element to be rotated around the z axis.
## Transisitions & Animations
  * for a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target pseudo-classes.
  * There are four transition related properties in total, including transition-property, transition-duration, transition-timing-function, and transition-delay. 
  * The transition-property property determines exactly what properties will be altered in conjunction with the other transitional properties. By default, all of the properties within an element’s different states will be altered upon change. However, only the properties identified within the transition-property value will be affected by any transitions.
  * It is important to note, not all properties may be transitioned, only properties that have an identifiable halfway point. Colors, font sizes, and the alike may be transitioned from one value to another as they have recognizable values in-between one another. The display property, for example, may not be transitioned as it does not have any midpoint. A handful of the more popular transitional properties include the following.
  * background - colorbackground - positionborder - colorborder - widthborder - spacingbottomclipcolorcropfont - sizefont - weightheightleftletter - spacingline - heightmarginmax - heightmax - widthmin - heightmin - widthopacityoutline - coloroutline - offsetoutline - widthpaddingrighttext - indenttext - shadowtopvertical - alignvisibilitywidthword - spacing
  * Transisiton duration - is the amount of time the transition takes place. 
  * Transition timing function - used to set the speed in which a transition will move. 
  * Transition Delay - setting a delay for the transition. 
  * Animation name - once the keyframes for an animation have been declared they need to be assigned a name to an element. 
  * Animation direction - On top of being able to set the number of times an animation repeats, you may also declare the direction an animation completes using the animation-direction property. Values for the animation-direction property include normal, reverse, alternate, and alternate-reverse.
  * Animation play state - The animation-play-state property allows an animation to be played or paused using the running and paused keyword values respectively. When you play a paused animation, it will resume running from its current state rather than starting from the very beginning again.
  * Animation fill mode - The animation-fill-mode property identifies how an element should be styled either before, after, or before and after an animation is run. The animation-fill-mode property accepts four keyword values, including none, forwards, backwards, and both.

## 8 Simple CSS3 transitions that will wow your users:
    * Fade in - are coded in two steps: first, you set the initial state; next you set the change. 
    * Change color - Now we just set the div's calss to color and specify the color we want in our CSS.
    * Grow and Shrink - To grow an element, you used to have to use its width and height, or its padding. But now we can use CSS3’s transform to enlarge.
    * Rotate Elements 
    * Square to circly - A really popular effect at the moment is transitioning a square element into a round one, and vice versa. With CSS, it’s a simple effect to achieve, we just transition the border-radius property.
    * 3D Shadow - achieved by adding a box shadow, and then moving the element on the x axis using the transform and translate properties so that it appears to grow out of the screen. 
    * Swing 
    * Inset border 

## 6 Buttons animated - 
