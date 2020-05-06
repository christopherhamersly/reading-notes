# Forms
  * There are several types of form controls that you can use to collect information from visitors to your site. 
  * Adding Text - text input (single line)
  * Password input - Like a single line text box but it masks the characters entered
  * text area - (multi-line)
  * radio forms, checkboxes, drop-down boxes, submit buttons, image buttons, file upload
* Users fill in a form and then presses a button to sumit the information to the server.  A form may have several form controls, each gathering different information. 

  * Form Structure - 
    1. < form > - form controls live inside a < form > element.
    1. action - every < form > element requires an action attribute. 
    1. method - forms can be sent using one of two methods. 
    1. id - the value is used to identify the form distinctly.
    1. size - the size attribute should not be used on new forms. 
  * Text Input
    1. < input > - used to create several different form controls.
    1. type = "text" - when the type attribute has a value of text, it creates single line text input
    1. name - when users enter information into a form, the server needs to know which form control each piece of data was entered into. 
    1. maxlength - you can use maxlength attribute to limit the number of characters a user may enter into the text field. 
  * Password Input
    1. < input > 
    1. type="password" - when the type attribute has a value of password it creates a text box that acts just like a single-line text input. 
    1. name - the name attribute indicates the name of the password input.
    1. size - maxlength - it can also carry the size and maxlength attributes. 
  * Text Area - used to create a multi line text input. 
  * Radio button 
    1. < input > 
      1. type = "radio"
      1. name
      1. value
      1. checked
  * Checkbox
    1. < input > - 
      * type="checkbox"
      * name
      * value
      * checked
  * Drop down list
    1. < select > - used to create the drop down list
      * Name
    1. < option > - used to specify the options that the user can select from. 
      * value
      * selected 
    1. < select >
      * size
      * multiple
    1. File input box
      * type="file" - creates a box that looks like a text input followed by a browse button
      * submit button
        1. type -"submit"
        1. name
        1. value
    1. Image button
      * type - "image"
        1. if you want to use an image for the submit button, you can give the type attribute a value of image. 
    1. Button and hidden controls
      * < button > 
      * < input >
    1. Labelling form controls
      * < label >
      * for
    1. Grouping form Elements 
      * < fieldset >
      * < legend >

#  Lists Tables and Forms
  * list-style-type - allows you to control the shape pr style of a bullet point.
  * list-style-image - you can specify an image to act as a bullet point using the list-style-image property. 
  * list-style-position - lists are indented into the page by default and the list-style-position property indicates whether the marker should appear on the inside or the outside of the box containing main points. 
    1. outside
    1. inside
  * list-style - shorthand
  * Table properties 
    1. width - to set the width
    1. padding - to set the space between the border of each table cell and its content
    1. text-transform - to convert the content of the table headers to uppercase
    1. letter-spacing, font-size
    1. border-top, border-bottom
    1. text-align
    1. background-color
    1. :hover
    * Empty cells
      1. show
      1. hide
      1. inherit  
  * Styling text inputs
    1. font-size
    1. color
    1. background-color
    1. border
    1. border-radius
    1. :focus
    1. :hover
    1. background-image
  * Styling submit buttons
    1. color
    1. text-shadow
    1. border-bottom
    1. background-color
    1. :hover
  * Styling fieldsets and legends
    1. width
    1. color
    1. background-color
    1. border
    1. border-radius
    1. padding
  * Cursor styles
    1. auto
    1. crosshair
    1. default
    1. pointer
    1. move
    1. text
    1. wait
    1. help
    1. url("cursor.gif")
    ***

* Javascript Events
  1. Different Event Types. 
  * UI Events
    * Load
    * unload
    * error
    * resize
    * scroll
  * Keyboard Events
    * keydown
    * keyup
    * keypress
  * Mouse Events
    * click
    * dblclick
    * mousedown
    * mouseup
    * mousemove
    * mouseover
    * mouseout
  * Focus Events
    * focus/focusin
    * blur/focusout
  * Form Events
    * input
    * change
    * submit
    * reset
    * cut
    * copy
    * paste
    * select
  * Mutation Events
    * DOMSubtreeModified
    * DOMNodeInserted
    * DOMNodeRemoved
    * DOMNodeInsertedIntoDocument
    * DomNodeRemovedFromDocument
  * How events trigger javascript code
    1. select the element node you want to respond to. - Select Element
    1. indicate which event on the selected node will trigger the respnd. - Specify Event
    1. State the code you want to run when the event occurs. - Call code
  * Three ways to bind an event to an element
    1. HTML Event Handlers
    1. Traditional DOM Event handlers
    1. DOM Level 2 Event Listeners
  * Event listeners - are a more recent approach tp handling events. 
  * Using parameters with event handlers & Listeners - because you cannot have paranthesis after the function names in event handlers or listeners, passing arguments requires a workaround. 
  * Using parameters with event listeners
  * Event Flow - HTML elements nest inside other elements. If you hover or click on a link, you will also be hovering or clicking on its parents elements. 
  * The event Object - when an event occurs, the event object tells you information about the event, and the element it happend upon. 
  * Event delegation - Creating event listeners for a lot of elements can slow down a page. 
  * Changing default behavior - preventDefault(), stopPropagation(), using both methods
  * Different types of events - W3C Dom events, HTML5 events, BOM events
  * User Interface events
    1. Load
    1. Unload
    1. error
    1. resize
    1. scroll
  * Keyboard events 
    1. input
    1. keydown
    1. keypress
    1. keyup
  * Form events
    1. submit
    1. change
    1. input
  * Mutation events and Observers
    1. DOMNodeInserted
    1. DOMNodeRemoved
    1. DOMSubTreeModified
    1. DOMNodeINsertedIntoDocument
    1. DOMNodeRemovedFromDocument
  * HTML5 Events
    1. DOMContentLoaded
    1. hashchange
    1. beforeunload
