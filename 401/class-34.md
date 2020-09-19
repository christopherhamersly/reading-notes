
# < Login  /> and < Auth />
### Questions
- Why is the Context API useful?
  - Context provides a way to pass data through the component tree without having to pass props down manually at every level
  - it provides a way for you to make particular data available to all components throughout the component tree no matter how deeply nested that component may be
- Can a component outside of a provider get its context?
- What are some common use cases for using the Context API?
  1. Themes
    >The ability to set the theme is one of the best UX. E.g medium provides dark mode and light mode which makes it easy to read in the low light situation.
    To implement themes, it is required to repaint every component with new color and change few images, if we do not use the context, it will be a chaos to repaint every component by passing new theme via props.
  1. Multilingual application
    >To implement multiple languages in app we have to change the text in every component and replace with the translated text. This can be easily implemented using Context.
    We can set the current language in the React context and all the components in a massive component tree can display text in the selected language. Using this we save prop drilling all the way down to the components.
  1. Authorisation: setting the user role and info
    This is one of the very common use cases. Many apps require to have dynamic content and messages based on the type of user has logged in. We can easily add User info in the Context and any component can pick info from a Context. We would be able to save all the prop drilling manually to all the levels.
- Describe “Context Hell”
  - This refers to the notion that React is a one way data structure.  This means that in order to pass down props to all of the children, it has to pass through the parents. Making code really sloppy and messy. 
***

### Terms

1. global state
  - when many components need access to the same stateful information, such as the current user's info or theme settings (light mode or dark mode).
1. global context
  - is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language. For example, in the code below we manually thread through a “theme” prop in order to style the Button component: class App extends React.
1. provider
  - makes the Redux store available to any nested components that have been wrapped in the connect() function. Since any React component in a React Redux app can be connected, most applications will render a < Provider > at the top level, with the entire app's component tree inside of it
1. consumer
  - A React component that subscribes to context changes. This lets you subscribe to a context within a function component. Requires a function as a child. The function receives the current context value and returns a React node.

*** 

### Resources 
[Resource 1](https://reactjs.org/docs/context.html#:~:text=Context.Consumer&text=A%20React%20component%20that%20subscribes,and%20returns%20a%20React%20node.)
[Resource 2](https://digitalguardian.com/blog/what-role-based-access-control-rbac-examples-benefits-and-more)
[Resource 3](https://www.npmjs.com/package/react-cookie)  