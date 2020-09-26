
# Redux - Combined Reducers
 Questions
1. Why choose Redux instead of the Context API for global state?
  - instead of importing actions and using them we get to manipulate the state directly on the component we are currently on. Context API is also easy to set up and is as effective as Redux
1. What is the purpose of a reducer?
  - Reducers specify how the application's state changes in response to actions sent to the store. Remember that actions only describe what happened, but don't describe how the application's state changes.
1. What does an action contain?
  - Actions are payloads of information that send data from your application to your store. They are the only source of information for the store. You send them to the store using store.dispatch().
1. Why do we need to copy the state in a reducer?
  - that every level of nesting must be copied and updated appropriately. This is often a difficult concept for those learning Redux, and there are some specific problems that frequently occur when trying to update nested objects. These lead to accidental direct mutation, and should be avoided.

***

### Terms

1. immutable state
  - is an object whose state cannot be modified after it is created. This is in contrast to a mutable object (changeable object), which can be modified after it is created.
1. time travel in redux
  - is the ability to move back and forth among the previous states of an application and view the results in real time. With Redux, given a specific state and a specific action, the next state of the application is always exactly the same.
1. action creator
  - s merely a function that returns an action object. ... Calling an action creator does nothing but return an object, so you have to either bind it to the store beforehand, or dispatch the result of calling your action creator.
1. reducer
  - is a function that determines changes to an application's state. It uses the action it receives to determine this change. ... Redux relies heavily on reducer functions that take the previous state and an action in order to execute the next state. We're going to focus squarely on reducers is in this post.
1. dispatch
  - s a function of the Redux store. You call store. dispatch to dispatch an action. This is the only way to trigger a state change. ... connect can accept an argument called mapDispatchToProps , which lets you create functions that dispatch when called, and pass those functions as props to your component.

*** 

### Resources 
[Resource 1](https://www.youtube.com/watch?v=gBER4Or86hE)
[Resource 2](https://redux.js.org/recipes/structuring-reducers/using-combinereducers/)
[Resource 3](https://redux.js.org/api/combinereducers/)  