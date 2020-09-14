

# Routing
 
1. Do child components have direct access to props/state from the parent?
  - They have anything that is passed in the body of the component. 
1. When a component “wraps” another component, how does the child component’s output  get rendered?
  - The wrapped component receives all the props of the container, along with a new prop, data , which it uses to render its output. The HOC isn't concerned with how or why the data is used, and the wrapped component isn't concerned with where the data came from.
1. Can a component, such as <Content />, which is a child also be used as a standalone component elsewhere in the application?
  -  Yes, by using React.fragment
1. What trick can a parent use to share all props with it’s children
  - You can React.Children to iterate over the children, and then clone each element with new props. You can also pass props to children with render props.  In this approach, the children is a function which can accept any arguments you want to pass and returns to the children. 

***

### Terms

1. props.children
  - children is a special property of React components which contains any child elements defined within the component, 

1. composition
  - is a natural pattern of the component model. It's how we build components from other components, of varying complexity and specialization through props.

*** 

### Resources 
[Resource 1](https://blog.pshrmn.com/simple-react-router-v4-tutorial/)
[Resource 2](https://www.freecodecamp.org/news/the-react-handbook-b71c27b0a795/#components)
 