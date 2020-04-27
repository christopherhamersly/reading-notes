# HTML
>When creating a web page, you add tags (known as markup) to the contents of the page.  
  >Two kinds of markup; Structural and Semantic.

## Structural Tags
##### Headings
- There are six levels of headings. Browsers display the contents of headings at different sizes.
  - >< h1 > , </ h1 >

  - >< h2 > , </ h2 >

  - >< h3 > , </ h3 >

##### Paragraphs
- Wrap text in a < p > tag to create new paragraphs
   - > < p > , </ p >

##### Bold and Italics
- Enclosing words in either < b >
/ < b > or < i > / < i > will make them either bold or italic.
  - bold < b >/ < b >
  - italic < i > / < i >  

##### Superscript & Subscript
- Wrapping words/letters with < sup > </ s u p > will make them a superscript.  Wrapping words/letters with < sub > </ sub > will make them a subscript

-  Creating a line break < br / > 

- Creating a horizontal horizontal line break < hr / >

## Semantic Markups
***

 - < strong > - makes the text bold

 - < em > - makes the text italics

 - < blockquote > - used for longer quotes that may take up an entire paragraph. 

 - < q > - used for shorter quotes that sit within a paragraph, browsers are supposed to put quotes around the element. 

 - < abbr > - if you use an abbreviation 

 - < cite > - used when referencing a piece of work such as a book, film or paper.  

 - < dfn > - Defining instance.  Should be used when using the term for the first time. 

 - < address > - The address element has quite a specific use: to contain contact details for the author of the page.

 - < ins > - Used to show content that has been inserted into a document. 

 - < del > - Strikethrough

 - < s > - Indicates that something is no longer relevant, but that it should not be deleted. 
 ***

 # CSS
 - Allows you to create rules that control the way each individual box is presented. 

 - Selectors - indicate which elements the rule applies to.  
 
 - Declarations - indicate how the elements referred to in the selector should be styled.  

 - Properties - indicate the aspects of the element you want to change. 

 - Values - Specify the settings you want to use for the chosen properties.
 ***  

 ### Using external CSS

 - < link > - can be used in an HTML document to tell the browser where to find the CSS file used to style a page. 

 - < href > - specifies the path to the CSS file

 - < type > - this attribute specifies the type of document being linked to.

 - < rel > - this specifies the relationship between the HTML page and the file its linked to.  

 - < style > - you can also include CSS rules within an HTML page by placing them inside a < style > 
 element
***
 #### CSS Selectors 
 - Universal selector - * { }
    >Applies to all elements in the document.

- Type selector - h1, h2, h3 { }
    > Targets the < h1 >, < h2 > and < h3 > tags

- Class selector - .note { } , p.note { }
    > targets any element whose class attribute has a value of note.
    > targets any element whose class attribute who has a value of note and p

- ID Selector - #introduction { }
    > targets the element whose ID attribute has a value of introduction

- Child Selector  - li>a { }
    >Matches an element that is a direct child of another 

- Descendant selector - p a { }
    > Matches an element that is the next sibling of another. 

- General sibling selector h1~ { }
    > Matches an element that is a sibling of another, although is does not have to be directly preceding element. 


# Javascript
>A script is a series of instructions that a computer can follow one-by-one. 

> Javascript is case sensitive

> You should write comments to explain what your code does. 

> Var is an example of what programmers call a keyword.  In order to use the variable, you must give it a name (This is also sometimes called an identifier)

>If a variable name is more than one word, it is usually written in camelCase.  

#### Data Types

> Numeric data types - 0.75

> String data type -'Hi, Ivy!'

> Boolean data type - true


#### Six Rules for naming variables.  

 1. The name must begin with a letter, dollar sign, or an underscore.  It must not start with a number. 
 1. The name can contain letters, numbers, dollar sign, or an underscore.  You may not use a dash or a dot in a variable name. 
 1. You cannot use **keywords** or **reserved** words.  Keywords are special words that tell the intepreter to do something. 
 1. All variables are case sensitive. 
 1. Use a name that describes the kind of information that the variable stores. 
 1. If our variable name is made up of more than one word, use a capital letter at the first letter of ever word *after* the first word. 

### Arrays
> A special type of variable.  It doesn't just store one value, it stores a list of values. 

> Values in an array are accessed as they are in a numbered list. It is important to know that the numbering of this list starts at zero (not one)

### Expressions 
> An expression evaluates into (results in) a single value.  Broadly speaking there are two types of expressions;
  > Expressions that just assign a value to a variable.
  > Expressions that use two or more values to return a single variable.  

### Operators 
> Assignment operators - assign a value to a variable

> Arithmetic operators - perform basic math

> String operators - combine two strings

> Comparision operators - compare two values and return trueor false

> Logical operators - combine expressions and return true or false. 

#### Arithmetic Operators

> Addition - + - Adds one value to another

> Subtration - - - Subtracts one value from another

> Division - / - Divides two values

> Multiplication - * - Multiplies two values using an asterick

> Increment - ++ - Adds one to the current number

> Decrement - -- - Subtracts one from the current number

> Modulus - % - Divides two values and returns the remainder

#### String Operators 

> There is just one string operator. The + symbol.  It is used to join the strings on either side of it. 

### Decisions and Loops

 - == is equal to
 - != is not equal to
 - === strictly equal to
 - !== strict not equal to
 - > greater than
 - < less than
 - >= greater than or equal to
 - <= less thanor equal to
 - && - (logical and) - this operator tests more than one condition
 - || - (logical not) - this operator takes a single Boolean value and inverts it. 
