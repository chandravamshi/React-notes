# react_hooks_notes
My understanding of react and notes I took during the process of understanding

---

### Introduction to React

Welcome to the world of React! In this guide, we'll explore the basics of React, including what it is, why it's used, its advantages, and how to get started with it.

### What is React?

React is a JavaScript library for building user interfaces. It allows you to create reusable UI components that efficiently update and render in response to data changes. Developed by Facebook and maintained by a community of developers, React simplifies the process of building complex user interfaces by breaking them down into smaller, reusable components.

### Why use React?

React makes it easier to develop interactive user interfaces by breaking them down into smaller, reusable components. It efficiently updates and renders components, resulting in faster performance and a better user experience. Its component-based architecture promotes code reusability and maintainability, while its virtual DOM implementation improves performance by minimizing DOM manipulations.

### Breaking User Interfaces into Smaller, Reusable Components:

Imagine you're building a house. Instead of building the entire house all at once, you break it down into smaller parts like rooms, walls, doors, and windows. Similarly, in React, you break down your user interface into smaller pieces called components. Each component represents a specific part of your UI, like a button, a form, or a header. These components can be reused throughout your application, just like using the same type of door in different rooms of a house. This makes your code easier to manage, update, and maintain.

### Efficiently Updating and Rendering Components:

When something changes in your application, React knows exactly which components need to be updated and re-rendered. Imagine you're playing a video game, and you pick up a new item. Only the part of the screen showing your inventory needs to change, not the entire game world. Similarly, React updates only the specific components that have changed, rather than re-rendering the entire page. This makes your application faster and more responsive, providing users with a better experience.

### Advantages of React Over Other Frameworks and Libraries:

React has several advantages over other JavaScript frameworks and libraries. It promotes a component-based architecture, which encourages code reusability and maintainability. Its virtual DOM implementation also improves performance by minimizing DOM manipulations. Some advantages of React include its component reusability, virtual DOM for efficient updates, and a large ecosystem of libraries and tools. However, React also has some disadvantages, such as a steep learning curve for beginners and potential performance issues with complex applications.

### Setting up a development environment with Create React App

To set up a development environment with Create React App:

1. Install Node.js and npm on your computer if you haven't already.
2. Open your terminal or command prompt.
3. Run `npm install -g create-react-app` to install Create React App globally.
4. Navigate to the directory where you want to create your React project.
5. Run `create-react-app your-project-name` to create a new React project.
6. Navigate into your project directory with `cd your-project-name`.
7. Run `npm start` to start the development server.
8. You can now start coding your React application!

### Conclusion

React is a powerful tool for building modern, interactive web applications. By breaking down user interfaces into smaller, reusable components and efficiently updating and rendering them, React provides a better development experience and improved performance. With Create React App, setting up a development environment is quick and easy, allowing you to focus on building great applications.

---

### Breaking User Interfaces into Smaller, Reusable Components

Imagine you're building a house. Instead of building the entire house all at once, you break it down into smaller parts like rooms, walls, doors, and windows. Similarly, in React, you break down your user interface into smaller pieces called components. Each component represents a specific part of your UI, like a button, a form, or a header. These components can be reused throughout your application, just like using the same type of door in different rooms of a house. This makes your code easier to manage, update, and maintain.

### Efficiently Updating and Rendering Components

When something changes in your application, React knows exactly which components need to be updated and re-rendered. Imagine you're playing a video game, and you pick up a new item. Only the part of the screen showing your inventory needs to change, not the entire game world. Similarly, React updates only the specific components that have changed, rather than re-rendering the entire page. This makes your application faster and more responsive, providing users with a better experience.

### Advantages of React Over Other Frameworks and Libraries

Think of React as a superhero that has special powers to make your development life easier. One of its superpowers is promoting a component-based architecture. This means you can build your application by piecing together reusable components like LEGO blocks. Just like how you can build different structures with the same LEGO pieces, you can create various UIs using the same React components.

Another superpower of React is its virtual DOM (Document Object Model). Imagine you have a blueprint of your house. Instead of physically moving furniture around to see how it looks, you make changes on a virtual copy of the blueprint. Once you're happy with the layout, you apply those changes to the actual house. Similarly, React creates a virtual representation of your UI in memory, compares it to the current DOM, and only updates the parts that have changed. This minimizes the number of updates to the actual DOM, resulting in faster performance.

In summary, React simplifies the process of building interactive user interfaces by breaking them down into smaller, reusable components. It efficiently updates and renders these components, resulting in faster performance and a better user experience. Its component-based architecture promotes code reusability and maintainability, while its virtual DOM implementation improves performance by minimizing DOM manipulations.

---
### How React's Virtual DOM Works

Let's break down how React's virtual DOM works step by step, using a simple example:

1. **Understanding the DOM:** The DOM (Document Object Model) is a representation of the structure of a web page. Think of it as a tree-like structure where each element (like `<div>`, `<p>`, `<span>`, etc.) is a node in the tree.

2. **Traditional DOM Manipulation:** In traditional web development, when you update something on a web page, the browser directly manipulates the DOM. For example, if you change the text of a paragraph (`<p>`), the browser updates that paragraph in the DOM, which can be slow and inefficient, especially for complex UIs.

3. **Introducing the Virtual DOM:** React introduces a concept called the virtual DOM. It's like a lightweight copy of the real DOM that React keeps in memory.

4. **Rendering Components to the Virtual DOM:** When you write React code, you create components that represent parts of your UI. When these components render, they don't directly update the real DOM. Instead, they update the virtual DOM.

5. **Diffing and Reconciliation:** After a component updates the virtual DOM, React performs a process called reconciliation. It compares the virtual DOM with the previous version of the virtual DOM to determine what has changed.

6. **Identifying Changes:** React identifies the differences between the new virtual DOM and the previous one. It figures out which parts of the UI need to be updated.

7. **Updating the Real DOM Efficiently:** Once React knows what has changed, it updates only those parts of the real DOM that need to be changed. This process is much faster than directly manipulating the entire DOM.

**Example:** Let's say you have a React component that displays a counter. When you click a button, the counter increases by one.

1. Initially, React renders the component and updates the virtual DOM with the initial counter value.
2. When you click the button, React updates the virtual DOM to reflect the new counter value.
3. React then compares the new virtual DOM with the previous one and identifies that only the counter value has changed.
4. Finally, React updates only the part of the real DOM that displays the counter, rather than re-rendering the entire page.

This process of using a virtual DOM allows React to efficiently update the UI, resulting in better performance, especially for complex applications with dynamic content.

---
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
In simple words, if you want to send variables through mutliple nested components we can use useContext.  
instead of sending variables as props to components you can simply use useContext hook.  
useContext provdes a way to pass data through component tree without passing data at each level of the tree.  
```
// firt create a Context
export const TestContext = React.createContext()  

// wrap a component with testContext provider
<TestContext.Provider value = {'testValue'}>
<ExampleComponet/>
<TestContext.Provider/>  

// Inside ExampleComponet
const testContext = useContext(TestContext)
return <div>{testContext}</div> // output testValue
```

##  TODO
### useRef 
### useMemo 
### useCallback 
### useLayoutEffect
### useImperativeHandle






  
