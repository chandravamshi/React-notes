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
* Example 1  
`const [count, setCount] = useState(0)`  
in the above code snippet count is a varialbe with intial value of 0 and setCount is a function.  
here count is a variable   
setCount is function 
`setCount` is a function which takes a callback function.  
`setCount((prevValue) => prevVlue +1)`  in this setCount will set the value to 1  
* Example 2 with object  
  `const [obj, setObj] = useState({firstName:'',lastName:''})`  
  `setObj({...obj, firstName:'Mynam'})` here `...obj` is spread spreading the obj valeus and overriding the firstName. If you don't spread the value of obj will have only `firstName`. same goes with arrays.

###  useEffect
used to perform side effects in FC.  
it is almost a replacement for componentDidUpdate,componentDidMount, componentDidUnmount in Class Component.  
runs after every render if no dependencies were given, renders when value of dependencies changes. will also have function insdie to run only before component will be unmounted. if empty array of dependencies provided runs only once only after component mounts.
return function is runned before component unmounts.

```
const [test, useTest] = useState(0)  

useEffect(
()=>{ // perfome something whenever test value changes}
 return () => 
 {
 // perform when component will unmount
} , [test] )
```   
###  useContext




  
