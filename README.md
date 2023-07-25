# react_hooks_notes
All Important react hooks explanations with examples.

## What are hooks and why hooks ?
It is a new feature from react 16.8 which allow you to use react features without writing a class.  
ex : state of component  
hooks don't work inside a class.  
#### why hooks?  
no need to create a class components.  
it will hlep to avoid the whole confusion with this keyword as you no longer use class components while using hooks.   
no need to bind event handlers like in class components.  
makes easy to share stat of the componets with other components.  
related code can be organized in one place.  
allow you to use reuse stateful logic.  
more readable and sufficient code accomplished using FC hooks.

#### Rules of hooks
only call hooks in top level of FC and any javascript funciton.  
don't call hooks in loops, condition or nested fucntions  


## hooks
###  useState
It is most common hook used. used to update a varialbe with simple steps.  
retuts a variable with initial value if given and function to udpate the varible.  
`const [count, setCount] = useState(0)`
here count is a variable   
setCount is function 
`setCount` is a function which takes a callback function.  
`setCount((prevValue) => prevVlue +1)`  in this setCount will set the value to 1
