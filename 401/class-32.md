
# Custom Hooks
### Questions
  - What does a component’s lifecycle refer to?
    - Each component in React has a lifecycle which you can monitor and manipulate during its three main phases. The three phases are:      
      > Mounting 
      > Updating  
      > Unmounting.
  - Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect
    - We do this because sometimes we need to use callback functions when a state is being changed or updating, depending on where else the function is being used in the app. 
  - Why are functional components preferred over class components?
    > Functional component are much easier to read and test because they are plain JavaScript functions without state or lifecycle-hooks. You end up with less code. They help you to use best practices.
  - What is wrong with the following code?
  <code>
  
  import React, {useState, useEffect} from 'react';

function MyComponent(props) {
  const [count, setCount] = useState(0);

  function changeCount(e) {
    setCount(e.target.value);
  }

  let renderedItems = []

  for (let i = 0; i < count; i++) {
    useEffect( () => {
      console.log('component mount/update');
    }, [count]);

    renderedItems.push(<div key={i}>Item</div>);
  }

  return (<div>
     <input type='number' value={count} onChange={changeCount}/>
      {renderedItems}
    </div>);
}
</code>

  - The above code is incorrect because it is calling the functions out of order. 

***

### Terms

1. state hook 
  - useState returns a pair: the current state value and a function that lets you update it. You can call this function from an event handler or somewhere else. It’s similar to this.setState in a class, except it doesn’t merge the old and new state together.1. effect hook
  - useEffect, adds the ability to perform side effects from a function component. It serves the same purpose as componentDidMount, componentDidUpdate, and componentWillUnmount in React classes, but unified into a single API.
1. reducer hook
  - An alternative to useState. Accepts a reducer of type (state, action) => newState, and returns the current state paired with a dispatch method. 

*** 

### Resources 
[Resource 1](https://www.telerik.com/kendo-react-ui/react-hooks-guide/#toc-custom-react-hooks)
