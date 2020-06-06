# Refactoring
  1. Functional programming is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data
  * Pure functions - 
  1. It returns the same result if given the same arguments (it is also referred as deterministic)
  1. It does not cause any observable side effects
  1. If our function reads external files, it’s not a pure function — the file’s contents can change.
  1. Any function that relies on a random number generator cannot be pure.
  1. Examples of observable side effects include modifying a global object or a parameter passed by reference.
  1. The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:
    >Given a parameter A → expect the function to return value B
    >Given a parameter C → expect the function to return value D
    >A simple example would be a function to receive a collection of numbers and expect it to increment each element of this collection.
  * Immutability - Unchanging over time or unable to be changed.
    > When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.
  * toLowerCase: converts the string to all lower case
  * trim: removes whitespace from both ends of a string
  *  split and join: replaces all instances of match with replacemen in    a given string. 

### pure functions + immutable data = referential transparency
  * Functions as first-class entities can:
    1. refer to it from constants and variables
    1. pass it as a parameter to other functions
    1. return it as result from other functions
  * Higher-order functions
    1. When we talk about higher-order functions, we mean a function that either:
    1. takes one or more functions as arguments, or
  returns a function as its result. 
  * Filter
    1. Given a collection, we want to filter by an attribute. The filter function expects a true or false value to determine if the element should or should not be included in the result collection. Basically, if the callback expression is true, the filter function will include the element in the result collection. Otherwise, it will not.
    1. A simple example is when we have a collection of integers and we want only the even numbers.
    1. Imperative approach
      > An imperative way to do it with Javascript is to:
        1. create an empty array evenNumbers
        1. iterate over the numbers array
        1. push the even numbers to the evenNumbers array
    1. Map
      >The idea of map is to transform a collection.
        * The map method transforms a collection by applying a function to all of its elements and building a new collection from the returned values.
    1. Reduce
      > The idea of reduce is to receive a function and a collection, and return a value created by combining the items

## Refactoring Javascript for performance
  1. Strategies
  > Here are some straightforward to implement methods that can lead to easier to read code. There are no absolutes when it comes to clean code — there's always an edge case!
    1.  Return early from functions:
    1. Cache variables so functions can be read like sentences:
    1. Check for Web APIs before implementing your own functionality:
    1. It's important to get your code right the first time because in many businesses there isn't much value in refactoring.
    1. 




