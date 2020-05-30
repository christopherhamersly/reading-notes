# Responsive Web Design

  ###  Responsive web Design is the practive of building a website suitable to work on every device and every screen size, no matter how large or small, mobile or desktop. 
  ***

    > There are three different ideas to consider when designing a site.  Responsive vs Adaptive vs Mobile.  

  #### Responsive generally means to to react quickly and positively to any change. 
  #### Adaptive means to be easily modified for a new purpose or sitatuation, such as change. 
  #### Mobile means to build out a seperate website commonly on a new domain solely for mobile users. 

  1. Flexible Layout - is the practice of building the layout of a website with a flexible grid, capable of dynamically resizing to any width.  Flexible grids are built using relative length units, most commonly percentages or em units.  These relative lengths are then used to declare common grid property values such as *width*, *margin*, or *padding*. 
    > Relative Viewport Lengths - 
      1. vw - viewports width
      1. vmin - minimum of the viewport's height and width
      1. vh - viewports height
      1. vmax - maximum of the viewports height and width

1. When using flexible layouts, definite amounts should be avoided.  Pixels, points, or inches should be replaced with em and percentages. You will be able to use this formula ( target / context = result ) to get the percentage that you will need to use to keep a flexible layout.

#### Media Queries - were built as an extension to media types commonly found when targeting and including styles.  Media queries provide the ability to specify different styles for indiviual browser and device circumstances, the width of a viewport or device orientation for example. 
  > using the @media rule inside of an existing style sheet, importing a new style sheet using the @import rule of by linking to a seperate style sheet from within the HTML document.  
  > there are many different selectors in the @media rule, some of them are; all, screen, print, tv, and braille, 3d glasses.  If a media type is not specified the default will be screen. 
  >There are three logical operators that can be used within the media queries.  *and*, *not*, and *only*. 
  > When using not and only logical operators the media type may be left off.  In this case the media type is defaulted to all. 

##### The most commonly used features within responsive design include min-width and max-width. 
  > Orientation Media Feature
  1. Determines if a device is in the landscape or portrait orientation.  The landscape mode is triggered when the display is wider than taller. 
  > Aspect ratio media features - features specifies the width/height pixel ratio of the targeted rendering area of output device.  The min and max prefixes are available to use with the different aspect ratio features. 
  > Pixel Ratio Media Features -  there are also pixel-ratio media features. These features do include the device-pixel-ratio feature as well as min and max prefixes. Specifically, the pixel ratio feature is great for identifying high definition devices, including retina displays. Media queries for doing so look like the following.
  > Resolution Media Feature - specifies the resolution of the output device in pixel density, also known as dots per inch or DPI. The resolution media feature does accept the min and max prefixes. Additionally, the resolution media feature will accept dots per pixel (1.3dppx), dots per centimeter (118dpcm), and other length based resolution values.

##### Mobile First
  1. One popular technique with using media queries is called mobile first.  The mobile first approach includes using style targeted at smaller viewports as the default styles for a website. 

***

## All about floats 
  > Float is a CSS positioning property. Floated elements remain a part of the flow of the web page. 
  > There are four valid float values for the float property.  Left and right float those elements those directions. None ensures the element will not float.  Inherit will assume the float value from that elements parent element. 
  > Floats can be used to create entire web layouts. 
  > Floats sister property is clear.  An element that has the clear property set on it will not move up adjacent to the float like the float desires, but will move itself down past the float. 
  > If the parent element contains nothing but floated elements, the height of it would literally collapse to nothing.  
  > Sometimes in order to gt around spacing issues when it comes to flexible viewing, you need to create a blank < div > section.  And inline style it to clear both floats.  
  > The Overflow Method relies on setting the overflow CSS property on a parent element. If this property is set to auto or hidden on the parent element, the parent will expand to contain the floats, effectively clearing it for succeeding elements. This method can be beautifully semantic as it may not require additional elements. However if you find yourself adding a new div just to apply this, it is equally as non-semantic as the empty div method and less adaptable. Also bear in mind that the overflow property isn’t specifically for clearing floats. Be careful not to hide content or trigger unwanted scrollbars.
  >The Easy Clearing Method uses a clever CSS pseudo selector (:after) to clear floats. Rather than setting the overflow on the parent, you apply an additional class like “clearfix” to it.
## Problems with Floats
  > Pushdown - is a symptom of an element inside a floated item being wider than the float itsefl.  Most browsers will render the image outside of the float, but have the part sticking out affect other layout. o
  > Quick Fixes to help with spacing. 
  1. overflow: hidden
  1. display:inline will get rid of the double margin bug
  

