
# React Native
 Questions
- Compare and Contrast Redux Toolkit with Redux “Ducks”
  > Redux Toolkit is our official, opinionated, batteries-included toolset for efficient Redux development. ... It also includes the most widely used Redux addons, like Redux Thunk for async logic and Reselect for writing selector functions, so that you can use them right away.
  > The basic idea behind Ducks is to create a file structure that is scalable and easy to follow. ... Using Redux to manage state results in copious numbers of actions that are used in multiple components and a state structure that is several levels deep.
  > Ducks is a modular pattern that collocates actions, action types and reducers.
  - According to the Ducks proposal:
  - A module…
    1. MUST export default a function called reducer()
    1. MUST export its action creators as functions
    1. MUST have action types in the form npm-module-or-app/reducer/ACTION_TYPE
    1. MAY export its action types as UPPER_SNAKE_CASE, if an external reducer needs to listen for them, or if it is a published reusable library

- What is the principle advantage of Redux Toolkit
  - Redux Toolkit was originally created to help address three common concerns about Redux:

    - "Configuring a Redux store is too complicated"
    - "I have to add a lot of packages to get Redux to do anything useful"
    - "Redux requires too much boilerplate code"
    - We can't solve every use case, but in the spirit of create-react-app and apollo-boost, we can provide an official recommended set of tools that handle the most common use cases and reduce the need to make extra decisions.

    - Redux Toolkit makes it easier to write good Redux applications and speeds up development, by baking in our recommended best practices, providing good default behaviors, catching mistakes, and allowing you to write simpler code. Redux Toolkit is beneficial to all Redux users regardless of skill level or experience. It can be added at the start of a new project, or used as part of an incremental migration in an existing project.

***

### Terms

1. redux toolkit slices 
  - A function that accepts an initial state, an object full of reducer functions, and a "slice name", and automatically generates action creators and action types that correspond to the reducers and state
1. namespace
  - In computing, a namespace is a set of signs (names) that are used to identify and refer to objects of various kinds. A namespace ensures that all of a given set of objects have unique names so that they can be easily identified.
  - Namespaces are commonly structured as hierarchies to allow reuse of names in different contexts. As an analogy, consider a system of naming of people where each person has a given name, as well as a family name shared with their relatives. If the first names of family members are unique only within each family, then each person can be uniquely identified by the combination of first name and family name; there is only one Jane Doe, though there may be many Janes. Within the namespace of the Doe family, just "Jane" suffices to unambiguously designate this person, while within the "global" namespace of all people, the full name must be used.


*** 

### Resources 
[Resource 1](https://reactnative.dev/docs/getting-started)
[Resource 2](https://reactnative.dev/docs/tutorial)
[Resource 3](https://reactnative.dev/) 