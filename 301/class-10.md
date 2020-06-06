# Javascript Call Stack
  1. A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc.
    > When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
    > Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
    > When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
    > If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.
    > The JavaScript engine (which is found in a hosting environment like the browser), is a single-threaded interpreter comprising of a heap and a single call stack. The browser provides web APIs like the DOM, AJAX, and Timers.
    > The call stack is primarily used for function invocation (call). Since the call stack is single, function(s) execution, is done, one at a time, from top to bottom. It means the call stack is synchronous.
    > In Asynchronous JavaScript, we have a callback function, an event loop, and a task queue. The callback function is acted upon by the call stack during execution after the call back function has been pushed to the stack by the event loop.
    > At the most basic level, a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).
    > Temporarily store: When a function is invoked (called), the function, its parameters, and variables are pushed into the call stack to form a stack frame. This stack frame is a memory location in the stack. The memory is cleared when the function returns as it is pop out of the stack.
    > Manage function invocation (call): The call stack maintains a record of the position of each stack frame. It knows the next function to be executed (and will remove it after execution). This is what makes code execution in JavaScript synchronous.
    > A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.
    > Types of error messages
    1. The first thing that indicates you that something is wrong with your code is the (in)famous error message that the one we saw just moments ago, it usually appears on your console (being developer tools of the browser, terminal or whatever else you are using).
    > Reference errors
    1. This is as simple as when you try to use a variable that is not yet declared you get this type os errors.
    1. Range errors
      > Try to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.
    1. To debug your JS code, the easiest and maybe the most common way its to simply console.log() the variables you want to check or, by using chrome developer tools, open your page with your JS code (press cmd+o in macOS or Ctrl+o in Windows) and choose your file to debug, click the line you wanna debug and refresh your page again (F5)
    1. You can also add conditional breakpoints by right-clicking a previous set breakpoint, which will make your program stop at that point only if a condition is met, this is awesome for when you want to debug huge cycles for specific values.
    1. testing is automatically called since it’s an IIFE (immediately Invoked Function Expression);
    1. obj variable is declared with the function add (using ES6 shorthand for functions in objects, it would be the same having var obj = { add: add } ;
    1. List of errors
      In this list, each page is listed by name (the type of error) and message (a more detailed human-readable error message). Together, these two properties provide a starting point toward understanding and resolving the error. For more information, follow the links below!

      1. Error: Permission denied to access property "x"
      1. InternalError: too much recursion
      1. RangeError: argument is not a valid code point
      1. RangeError: invalid array length
      1. RangeError: invalid date
      1. RangeError: precision is out of range
      1. RangeError: radix must be an integer
      1. RangeError: repeat count must be less than infinity
      1. RangeError: repeat count must be non-negative
      1. ReferenceError: "x" is not defined
      1. ReferenceError: assignment to undeclared variable "x"
      1. ReferenceError: can't access lexical declaration`X' before initialization
      1. ReferenceError: deprecated caller or arguments usage
      1. ReferenceError: invalid assignment left-hand side
      1. ReferenceError: reference to undefined property "x"
      1. SyntaxError: "0"-prefixed octal literals and octal escape seq. are deprecated
      1. SyntaxError: "use strict" not allowed in function with non-simple parameters
      1. SyntaxError: "x" is a reserved identifier
      1. SyntaxError: JSON.parse: bad parsing
      1. SyntaxError: Malformed formal parameter
      1. SyntaxError: Unexpected token
      1. SyntaxError: Using //@ to indicate sourceURL pragmas is deprecated. Use //# instead
      1. SyntaxError: a declaration in the head of a for-of loop can't have an initializer
      1. SyntaxError: applying the 'delete' operator to an unqualified name is deprecated
      1. SyntaxError: for-in loop head declarations may not have initializers
      1. SyntaxError: function statement requires a name
      1. SyntaxError: identifier starts immediately after numeric literal
      1. SyntaxError: illegal character
      1. SyntaxError: invalid regular expression flag "x"
      1. SyntaxError: missing ) after argument list
      1. SyntaxError: missing ) after condition
      1. SyntaxError: missing : after property id
      1. SyntaxError: missing ; before statement
      1. SyntaxError: missing = in const declaration
      1. SyntaxError: missing ] after element list
      1. SyntaxError: missing formal parameter
      1. SyntaxError: missing name after . operator
      1. SyntaxError: missing variable name
      1. SyntaxError: missing } after function body
      1. SyntaxError: missing } after property list
      1. SyntaxError: redeclaration of formal parameter "x"
      1. SyntaxError: return not in function
      1. SyntaxError: test for equality (==) mistyped as assignment (=)?
      1. SyntaxError: unterminated string literal
      1. TypeError: "x" has no properties
      1. TypeError: "x" is (not) "y"
      1. TypeError: "x" is not a constructor
      1. TypeError: "x" is not a function
      1. TypeError: "x" is not a non-null object
      1. TypeError: "x" is read-only
      1. TypeError: 'x' is not iterable
      1. TypeError: More arguments needed
      1. TypeError: Reduce of empty array with no initial value
      1. TypeError: X.prototype.y called on incompatible type
      1. TypeError: can't access dead object
      1. TypeError: can't access property "x" of "y"
      1. TypeError: can't assign to property "x" on "y": not an object
      1. TypeError: can't define property "x": "obj" is not extensible
      1. TypeError: can't delete non-configurable array element
      1. TypeError: can't redefine non-configurable property "x"
      1. TypeError: cannot use 'in' operator to search for 'x' in 'y'
      1. TypeError: cyclic object value
      1. TypeError: invalid 'instanceof' operand 'x'
      1. TypeError: invalid Array.prototype.sort argument
      1. TypeError: invalid arguments
      1. TypeError: invalid assignment to const "x"
      1. TypeError: property "x" is non-configurable and can't be deleted
      1. TypeError: setting getter-only property "x"
      1. TypeError: variable "x" redeclares argument
      1. URIError: malformed URI sequence
      1. Warning: 08/09 is not a legal ECMA-262 octal constant
      1. Warning: -file- is being assigned a //# sourceMappingURL, but already has one
      1. Warning: Date.prototype.toLocaleFormat is deprecated
      1. Warning: JavaScript 1.6's for-each-in loops are deprecated
      1. Warning: String.x is deprecated; use String.prototype.x instead
      1. Warning: expression closures are deprecated
      1. Warning: unreachable c      1. ode after return statement
