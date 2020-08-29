# Class 02

### Name 3 advantages to Test Driven Development
  - Code flexibility and easier maintenance.
  - With TDD you will get a reliable solution.
  - Save project costs in the long run.

In what case would you need to use beforeEach() or afterEach() in a test suite? 
  - The before and after will run before and after the execution of the test suite respectively (in our case, the test-file), while beforeEach and afterEach are ran before and after each test case (test step).

What is one downside of Test Driven Development 
  - It necessitates a lot of time and effort up front, which can make development feel slow to begin with. Focusing on the simplest design now and not thinking ahead can mean major refactoring requirements. (https://leantesting.com/test-driven-development/#:~:text=It%20necessitates%20a%20lot%20of,essentials%20and%20avoid%20the%20superfluous.)

What’s the primary difference between ES6 Classes and Constructor/Prototype Classes? 
  - A child of an ES6 class is another type definition which extends the parent with new properties and methods, which in turn can be instantiated at runtime. A child of a prototype is another object instance which delegates to the parent any properties that aren't implemented on the child. (https://www.toptal.com/javascript/es6-class-chaos-keeps-js-developer-up#:~:text=A%20child%20of%20an%20ES6,t%20implemented%20on%20the%20child.)

Name a use case for a static method 
  - We can also assign a method to the class function itself, not to its "prototype". (https://javascript.info/static-properties-methods)

Write an example of a Higher Order function and describe the use case it solves A higher order function is a function that takes a function as an argument, or returns a function

  - const startsWithS = words => { const filtered = []; for (let i = 0, { length } = words; i < length; i++) { const word = words[i]; if (word.startsWith('s')) filtered.push(word); } return filtered; }; 
  
  startsWithS(['oops', 'gasp', 'shout', 'sun']); // [ 'shout', 'sun' ]

  Returns all of the words that start with S.

*** 

### Terms

1. functional programming 
  - is a programming paradigm where programs are constructed by applying and composing function 
1. pure function 
  - The function always returns the same value for the same inputs. Evaluation of the function has no side effects. Side effects refer to changing other attributes of the program not contained within the function, such as changing global variable values or using I/O streams
  higher-order function (https://medium.com/better-programming/what-is-a-pure-function-3b4af9352f6f)   
1. immutable state
 - is an object whose state cannot be modified after it is created. 
1. object
  -  everything in javascript is an object. 
1. object-oriented programming (OOP) 
  - is a computer programming model that organizes software design around data, or objects, rather than functions and logic. An object can be defined as a data field that has unique attributes and behavior. 
  (https://searchapparchitecture.techtarget.com/definition/object-oriented-programming-OOP#:~:text=Object%2Doriented%20programming%20(OOP)%20is%20a%20computer%20programming%20model,has%20unique%20attributes%20and%20behavior.) 
1. class 
  -  A class is written by a programmer in a defined structure to create an object (computer science) in an object oriented programming language. (https://simple.wikipedia.org/wiki/Class_(programming)#:~:text=A%20class%20is%20written%20by,all%20objects%20of%20one%20type.) 
1. prototype 
  - The JavaScript prototype property allows you to add new properties to object constructors: 
  (https://www.w3schools.com/js/js_object_prototypes.asp) 
1. super 
  - used to access and call functions on an object's parent. https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/super 
1. inheritance 
  - child classes take on all of the prototypes from the parent classes.
1. constructor 
  -  sets all of the parameters and defines what methods are attached to all of the objects. 
1. instance 
  - can be used informally to mean an object created using a particular constructor function. 
1. context 
  -  refers to the object to which a function belongs. this - refers to the object it belongs to. 
1. Test Driven Development (TDD) 
  -  is a software development process that relies on the repetition of a very short development cycle: requirements are turned into very specific test cases, then the code is improved so that the tests pass. This is opposed to software development that allows code to be added that is not proven to meet requirements. 
  (https://en.wikipedia.org/wiki/Test-driven_development) 
1. Jest 
  -  a delightful JavaScript Testing Framework with a focus on simplicity. (https://jestjs.io/) 
1. Continuous Integration (CI) 
  -  is the practice of merging all developers' working copies to a shared mainline several times a day. unit test - is a software testing method by which individual units of source code—sets of one or more computer program modules together with associated control data, usage procedures, and operating procedures—are tested to determine whether they are fit for use. (https://en.wikipedia.org/wiki/Unit_testing)