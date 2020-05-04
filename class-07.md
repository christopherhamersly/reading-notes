# Tables 
  * A table represents information in a grid format.  Examples of tables include financial reports, TV schedules. and sports results.

  * Basic table structure 
    1. < table > - used to creat a table.
    1. < tr > - the indication of a new row
    1. < td > - the cell of a table
    1. < th > - used just like a td element but its purpose is to represent the heading for either a column or a row. 
    1. < colspan > - tells the HTML how many rows it needs to run through
    1. < rowspan > - works much like the colspan tag. 
    1. < thead > - the heading of a table should sit inside this tag.
    1. < tbody > - the body should sit inside this tag. 
    1. < tfoot > - the footer belongs in this element
    
  ***

# Javascript 

  * Updating an object 
    1. to update the value of properties, use dot notation or square brackets.  They work on objects created using literal or constructor notation. To delete a property, use the delete keyword. 
  * Constructor notation 
    1. sometimes you will want several objects to represent similiar things. Object constructors can use a function as a template for creating objects. 
    1. You create instances of the object using the contructor function. The new keyword followed by a call to the function
  * The Keyword this is commonly used inside functions and objects. Where the function is declared alters what this means.  It always refers to one object, usually the object in which the function operates. 
  * Javascript stores using name/value pairs.  To organize your data, you can use an array or object to group a set of related values. 
    > Arrays are objects.  
      * They hold a related set of key/value pairs, but the key for each value is its index number.  

  * Three groups of built in objecuts
    - Browser object model - creates a model of the browser tab or window
    - Document object model - creates a model of the current web page
    - Global Javascript object - The global object do not form a single model.  They are a group of individual objects that relate to different parts of the Javascript language. 

  ### The browser object model 
  * Properties
    * window.innerHeight
    * window.innerWidth
    * window.pageXOffset
    * window.pageYOffest
    * window.screenX
    * window.screenY
    * window.location
    * window.document
    * window.history
    * window.history.lenght
    * window.screen
    * window.screen.width
    * window.screen.height
  * Methods
    * window.alert()
    * window.open()
    * window.print()

  ### the document object model
  * Properties
    * document.title
    * document.lastModified
    * document.URL
    * document.domain
  
  * Method
    * document.write()
    * document.gtElementById()
    * document.querySelectorAll()
    * document.createElement()
    * document.createTextNode()

  #### Global Object
    * String Objects 
      * properties
        * length
      
      * methods
        * toUpperCase()
        * toLowerCase()
        * charAt()
        * indexOf()
        * lastIndexOf()
        * substring()
        * split()
        * trim()
        * replace()
        * saying.length;
        
    * Number Object 
      * inNan() - checks if the value is not a number
      * toFixed() - rounds to specified number of decimal places 
      * toPrecision() - rounds to total number of places
      * toExponential - returns a string representing the number in exponential notation
    
    * Math Object
      * Math.PI - returns pi
      * Math.round() - rounds number to larges integer
      * Math.sqrt() - returns square root of positive number
      * Math.ceil() - rounds up to the nearest integer
      * Math.floor - rounds number down to the nearest integer
      * Math.Random - generates a random number between 0 (inclusive) and 1 (not inclusive)

    * Date object
      * getDate()
      * getDay()
      * getFullYear()
      * getHours()
      * getMilliseconds()
      * getMinutes()
      * getMonth()
      * getSeconds()
      * getTime()
      * getTimezoneOffset()
      * toDateString()
      * toTimeString()
      * toString()