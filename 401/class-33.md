

# Context API
### Questions
- Describe use cases for useMemo() and useReducer()
  - useMemo()
    > A use case for useMemo is when the user is dealing with very large function calls that may take a long time to render, or to compute.  We don't want the user to have to wait for elements on a page to load, so we can use this method to help expedite the process. 
  - useReducer()
    > This could be used when one state is waiting on the next value to populate.  Kind of similiar to an async and await function call. 
- Why do custom hooks need the use prefix?
  - This is mainly to have an extra option for sharing state and logic between components.
- What do custom hooks usually do?
  - Custom hooks can be used to encapsulate common state-full functions for use in other hooks.
- Using any list of custom hooks, research and name one that you think    will be useful in your applications
  - useDarkMode - Although I don't necessarily think it is the most useful hook, I think it would be neat to be able to find a way to implement this hook. 
- Describe how a hook that fetches API data might work
  - It would take in an async function as an input and return the value, error, and status values we need to properly update our UI. 
***
- Which 3 things had you heard about previously and now have better clarity on?
  - Have a little bit of a better understanding of how hooks work. 
  -  Feel a little more confident knowing there are so many recipes that are able to be used in the world. 
  - Also, nice to know there are some built in methods to react, that way we don't have to create all of our methods from scratch. 

- What are you most excited about trying to implement or see how it works?
  - Tracking the hooks progress and actually seeing it in action. 
### Terms

1. reducer
  -  are there to manage state in an application. For instance, if a user writes something in an HTML input field, the application has to manage this UI state 

*** 

### Resources 
[Resource 1](https://medium.com/better-programming/quick-intro-to-react-hooks-6e8a44ae4aa6#:~:text=Custom%20Hooks,-Here's%20where%20the&text=This%20is%20mainly%20to%20have,state%20and%20logic%20between%20components.&text=Custom%20hooks%20are%20normal%20JS,be%20reused%20in%20other%20components.)
 