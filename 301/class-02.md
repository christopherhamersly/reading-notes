# jQuery, Events, and the DOM

  ## jQuery offers a simple way to achieve a variety of common Javascript tasks quickly and consistently, across all major browsers and without any fallback code needed. 
  >jQuery helps select elements, perform tasks, and handle events more easily. 
  > $ will now replace writing out jQuery. 
  > $('li.hot') targets all of the li elements with a class of hot. 
  > The jQuery object has many methods that you can use to work with the elements you select.  The methods represent tasks you commonly need to perform with elements. 
  > $('li.hot).addClass('complete'); = this adds a class of complete to the 'li.hot' class.  
  > In order to use jQuery much like javascript you have to add the script to the HTML page, in the same place you would include javascript.  At the bottom of the HTML page, but still inside the body. 
  > jQuery doesn't do anything you cannot achieve with pure Javascript.  It is just a Javascript file. Its more widely used becasue it makes coding simpler.  With the following; 
    1. simple selectors
    2. common tasks in less code
    3. cross-browser compatability
  > jQuery can be used to select just one object, or it can be used to select multiple things from the DOM.  jQuery returns multiple objects back in an array.
  > Some jQuery methods both retrieve information from, and update the contents of, elements.  But they do not always apply to all elements. 
  > When you create a selection with jQuery, its stores a reference to the corresponding nodes in the DOM tree.  It does not create copies of them. 
  > A jQuery object stores references to elements.  Catching a jQuery object stores a reference to  it in a variable. 
  > In order to save working memory in the CPU as programmers, many times jQuery objects will be stored in a variable, often starting with the $ to denote it is a jQuery reference. 
  > Unlike javascript, where you have to run loops over information, jQuery allows the user to use implicit iteration in order to update information. 
  > Chaining jQuery is the process of placing several methods in the same selector,using dot notation. 
  > Getting element content = 
  1. .html() - when this method is used to retrieve information from a jQuery selection, it retrieves only the HTML inside the first element in the matched set, along with any of its decendants. 
  1. .text() - when this method is used to retrieve the text from a jQuery selection, it returns the content from every element in the jQuery selection along with the text from any decendants. 

  #### Updating Elements - four elements are used to update elements 
    1. html()
    1. .text()
    1. .replaceWth()
    1. .remove()
  > Inserting elements involves two steps:
  1. Create new elements in a jQuery object
  2. Use a method to insert the content into that page
  > Getting and setting attribute values - you can create attributes, or access and update their contents, using the following four methods;
  1. .attr()
  1. .addClass()
  1. .removeAttr()
  1. .removeClass()
  > Getting and setting CSS properties - the .css() method lets you retrieve and set the values of CSS properties. 
  > jQuery also handles event methods as well, by using the 'on' command.  This object can use the following properties;
    1. type
    1. which
    1. data
    1. target
    1. pageX
    1. pageY
    1. timeStamp
    
### Loading jQuery from a CDN
  > known as a content delivery network - is a series of servers spread out around the world.  

## Six Reasons for pair programming
  > While learning to code, developers likely study several programming languages. Similar to a foreign language class, there are four fundamental skills that help anyone learn a new language: Listening: hearing and interpreting the vocabulary Speaking: using the correct words to communicate an idea Reading: understanding what written language intends to convey Writing: producing from scratch a meaningful
  > They also help with the following; greater efficiency, engaged collaboration, learning from fellow students, social skills, job interview readiness, work environmnent readiness.
  
  