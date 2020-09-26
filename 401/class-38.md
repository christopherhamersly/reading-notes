
# Redux - Asynchronous Actions
 Questions
1. How granular should your reducers be?
  - Reducer functions should only depend on their state and action arguments, and should only calculate and return a new state value based on those arguments. They must not execute any kind of asynchronous logic (AJAX calls, timeouts, promises), generate random values (Date.now(), Math.random()), modify variables outside the reducer, or run other code that affects things outside the scope of the reducer function.
1. Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched
  - I feel like this is a pro.  This allows you the user to set up a reducer, and leave it. 

1. Name a strategy for preventing the above
  - Avoid putting non-serializable values such as Promises, Symbols, Maps/Sets, functions, or class instances into the Redux store state or dispatched actions. This ensures that capabilities such as debugging via the Redux DevTools will work as expected. It also ensures that the UI will update as expected.
***

### Terms

1. store
  -  holds the whole state tree of your application. The only way to change the state inside it is to dispatch an action on it. A store is not a class. It's just an object with a few methods on it.
1. combined reducers
  - The combineReducers helper function turns an object whose values are different reducing functions into a single reducing function you can pass to createStore.

  - The resulting reducer calls every child reducer, and gathers their results into a single state object. The state produced by combineReducers() namespaces the states of each reducer under their keys as passed to combineReducers()

*** 

### Resources 
[Resource 1](https://redux.js.org/advanced/async-actions)
[Resource 2](https://github.com/reduxjs/redux-thunk)
[Resource 3](https://www.digitalocean.com/community/tutorials/redux-redux-thunk)  