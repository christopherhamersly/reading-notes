# Event Driven Programming

-  Event Driven Progamming 
  -  is a logical pattern that we can choose to confine our programming within to avoid issues of complexity and collision.
- Event-Driven Programming makes use of the following concepts:

  - An Event Handler is a callback function that will be called when an event is triggered.
  - A Main Loop listens for event triggers and calls the associated event handler for that event.

 - EventEmitter
  - We access the EventEmitter class through the events module. Once imported we’ll need to create a new object from the class to start using it.
  
    > `  const EventEmitter = require('events').EventEmitter;
    const myEventEmitter = new EventEmitter;   ` 

-  We’ll need an event listener for a userJoined event. First, we’ll write a function that will act as our event listener, then we can use EventEmitters on method to set the listener.

    > `  const EventEmitter = require('events').EventEmitter;
        const chatRoomEvents = new EventEmitter;
      function userJoined(username){
      // Assuming we already have a function to alert all users.
      alertAllUsers('User ' + username + ' has joined the chat.');  `
      }

      // Run the userJoined function when a 'userJoined' event is triggered.
      chatRoomEvents.on('userJoined', userJoined);

- The next step would be to make sure that our chat room triggers a userJoined event whenever someone logs in so that our event handler is called. EventEmitter has an emit method that we we use to trigger the event. We would want to trigger this event from within a login function inside of our chatroom module.

    > `function login(username){
      chatRoomEvents.emit('userJoined', username);
      }`

- To remove event listeners in EventEmitter we can use the removeListener or removeAllListeners method. It’s important to note that in the EventEmitter that comes built-in with Node you must pass a reference to the exact function you wish to remove when using the removeListener method. This means wherever you wish to remove the event, you’ll need to make sure the function is able to be referenced from that place in your code. For this reason it is often best to name your event handling functions and declaring them before you register the event listener, as opposed to leaving them anonymous.

    > `const EventEmitter = require('events').EventEmitter;
const chatRoomEvents = new EventEmitter; 
function userJoined(username){
  chatRoomEvents.on('message', function(message){
    document.write(message); 
  })
}
chatRoomEvents.on('userJoined', userJoined)  `

All of that headache can be avoided if we rewrite the code like so:

  >  `  const EventEmitter = require('events').EventEmitter;
const chatRoomEvents = new EventEmitter;
function displayMessage(message){
  document.write(message);
}
function userJoined(username){
  chatRoomEvents.on('message', displayMessage);
}
chatRoomEvents.on('userJoined', userJoined); `

- Now if we want to remove the displayMessage function from the message event’s list of handlers:
  > ` chatRoomEvents.removeListener('message', displayMessage); `


- The Object Oriented approach promotes the idea that all behavior of an individual unit (or object) be handled from code within that unit. Using this approach, applications are built with many different units that all speak to and interact with each other.

- Imagine we’re building a mail application. We might have an object whose sole purpose is to process the incoming and outgoing mail messages for our client. This object would contain all of its own behavioral functions. We might have a sendMail function that delivers our mail to a server. We might also have a receiveMail function that tells the server to deliver us any new mail it has for us. We’ll call the object responsible for these server interactions our Mailbox.
  > `const Mailbox = {
  sendMail: function(){
    // code to send mail.
  },
  receiveMail: function(){
    // check server for new mail.
  }
}`

- Now if we are building other units that want to make use of our sendMail function, they can access it through Mailbox.sendMail
  > `class Food {
  constructor(name) {
    this.name = name;
  }
  becomeEaten() {
    return 'I have been eaten.';
  }
}
var bacon = new Food('bacon');
class gator {
  eat() {
    bacon.becomeEaten();
  }
}` 

- In this example, our gator had to access the methods inside of Food in order to eat. This is a lot of work for our lazy gator so we’re going to make things easier for him.
  > ` const EventEmitter = require('events').EventEmitter;
const myGatorEvents = new EventEmitter;
class Food {
  constructor(name) {
    this.name = name;
    // Become eaten when gator emits 'gatorEat'
    myGatorEvents.on('gatorEat', this.becomeEaten);
  }
  becomeEaten(){
    return 'I have been eaten.';
  }
}
var bacon = new Food('bacon');
const gator = {
  eat() {
    myGatorEvents.emit('gatorEat');
  }
} `

- Now all our gator has to do is just say gatorEat and the EventEmitter takes care of the rest.

