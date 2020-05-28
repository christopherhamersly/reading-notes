# Java Script Debugging
  1. Java script works top to bottom.  Start at the top and work your way down.  
  1. Each time a script enters a new excecution context, there are two phases of activity:
    > Prepare - The new scope is createed
    > Excecute - Now it can ssign values to variables.  
    > In the interpreter, each excecution context has its own variables object. 
  1. Understanding Errors;
    1. If a javascript statement generates an error, then it throws an exception.  At that point, the intepreter stops and looks for exception handling code. 
    1. Error objects - Can help you find where your misteks are and browsers have tools to help you read them. 
      1. name - type of exceution
      1. message - description
      1. fileNumber - name of the Javascript File
      1. lineNumber - Line number of error.
      1. error - generic error- the other errors are all based upon this error. 
      1. syntax error - syntax has not been followed. 
      1. ReferenceError - Tried to reference a variable that is not declared/within scope. 
      1. Type Error - An unexpected data type that cannot be coerced
      1. Range Error - Numbers are in acceptable range
      1. URI Error - encodeURI(), decode(), and simliar methods used incorrectly
      1. EvalError - eval() function usd incorrectly. 
      1. SyntaxError - syntax is not correct
      1. ReferenceError - variable does not exist
      1. TypeError - value is unexpected data type
      1. RangeError - number outside of range
  1. How to deal with errors
    1. debug the script to fix errors
    1. handle errors gracefully - using try, catch, throw, and finally statements
  1. A debugging workflow -
    1. Where is the problem. 
    1. What exactly is the problem. 
  * How to look at errors in Chrome - 
    1. the console will show you when there is an error in your Javascript.  It also displays the line where it became a problem for the interpreter. 
  * How to look at errors in Firefox - follow same directions as chrome. 
  * Logging information into the console log for different lines of code will help to sort out where the error is occuring. 

  * Breakpoints
  1. You can pause the excecution of a script on any line using breakpoints  Then you can check the values stored in variables at that point in time. 
  1. Stepping through code - If you set mulitple breakpoints, you can step through them one-by-one to see where values change anda problem might occur. 

  * Conditional Breakpoints - You can indicate that a breakpoint should be triggered only if a condition that you specify is met.  The condition can use existing variables. 
    1. Debugger Keyword - You can create a breakpoint in your code using just the debugger keyword.  When the developer tools are open, this will automatically cause a breakpoint. 
  * handling Exceptions - if you know your code might fail; use, try, catch, and finally.  
  
  * Debugging Tips - Another browser, add numbers, strip it back, explaining the code, search, code playgrounds, validation tools, go back to basics, 
  