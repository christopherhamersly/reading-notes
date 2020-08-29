# TCP Servers


- Why are events sometimes better than asynchronous actions with callbacks? 
  > Usually the myaction program will run as an independent thread or even a separate process. While the "event handler" pattern is more complex it is much more robust and less likely to hang when an action fails. It also makes for a more responsive GUI. A callback is procedure you pass as an argument to another procedure.
- What does an EventEmitter instance do?
  >All objects that emit events are instances of the EventEmitter class. These objects expose an eventEmitter. on() function that allows one or more functions to be attached to named events emitted by the object. ... The following example shows a simple EventEmitter instance with a single listener.
- When is a program’s call stack, event queue, and event loop active?
  > While our code is being invoked, the event loop periodically checks if the call-stack is empty. Once the call-stack has run all the execution contexts in our code, the event loop takes the first function that entered the callback queue and places it on the call-stack to be executed

***

### Terms 
1. Observer Pattern - offers a subscription model in which objects subscribe to an event and get notified when the event occurs.
1. Listener -  is a procedure in JavaScript that waits for an event to occur. The simple example of an event is a user clicking the mouse or pressing a key on the keyboard.
1. Event Handler -  can be used to handle, and verify, user input, user actions, and browser actions: Things that should be done every time a page loads. Things that should be done when the page is closed. Action that should be performed when a user clicks a button. Content that should be verified when a user inputs data.
1. Event Driven Programming - Event-driven programming with JavaScript is a useful way to create interactive websites. Typically, after the webpage has loaded the JavaScript program continues to run waiting for an event. If you connect this event to a JavaScript function then the function will run when the event occurs.
1. Event Loop - The event loop is the secret behind JavaScript's asynchronous programming. JS executes all operations on a single thread, but using a few smart data structures, it gives us the illusion of multi-threading. Let's take a look at what happens on the back-end.
1. Event Queue - JavaScript runtimes contain a message queue which stores a list of messages to be processed and their associated callback functions
1. Call Stack - A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc
1. Emit/Raise/Trigger - These are all methods use to set off an event.
1. Subscribe - The subscriber function defines how to obtain or generate values or messages to be published. To execute the observable you have created and begin receiving notifications, you call its subscribe() method, passing an observer
1. Database - The storage mechanism. 


*** 
### Resources 
  -  [Resource 1](https://dev.to/thebabscraig/the-javascript-execution-context-call-stack-event-loop-1if1#:~:text=While%20our%20code%20is%20being,call%2Dstack%20to%20be%20executed)

  - [Resource 2](https://nodejs.org/api/events.html#:~:text=All%20objects%20that%20emit%20events,events%20emitted%20by%20the%20object.&text=The%20following%20example%20shows%20a%20simple%20EventEmitter%20instance%20with%20a%20single%20listener)

  - [Resource 3](https://stackoverflow.com/questions/2069763/difference-between-event-handlers-and-callbacks#:~:text=Usually%20the%20myaction%20program%20will,for%20a%20more%20responsive%20GUI.&text=A%20callback%20is%20procedure%20you%20pass%20as%20an%20argument%20to%20another%20procedure)