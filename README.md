# React Notes
My Understanding of React and Learning Notes

---
## Table of Contents
* [Basic short intro to React](#basic-short-intro-to-react)
* [Introduction to React](#introduction-to-react)
* [Breaking User Interfaces into Smaller, Reusable Components](#breaking-user-interfaces-into-smaller-reusable-components-1)
* [How React's Virtual DOM Works](#how-reacts-virtual-dom-works)
* [JSX](#jsx)
* [Creating and Rendering Components](#creating-and-rendering-react-components)
* [Props and State](#props-and-state-in-react)
* [Handling Events](#handling-events-in-react)
* [Lists and Keys](#lists-and-keys-in-react)
* [Conditional Rendering](#conditional-rendering)
* [Forms and Controlled Components](#forms-and-controlled-components)
* [Lifecycle Methods in Class Components](#lifecycle-methods-in-class-components)
* [Hooks](#hooks)
     * [useState](#useState)
     * [useEffect](#useEffect-hook)
     * [useEffect](#useEffect-hook)
     * [Context and useContext Hook](#context-and-useContext-hook)
---

## Short intro to React
1. **Introduction to React:**
   - React is a JavaScript library for building user interfaces.
   - It allows us to create reusable UI components that update efficiently when data changes.
   - React uses a virtual DOM to improve performance by minimizing the number of changes to the actual DOM.

2. **Components:**
   - Components are the building blocks of React applications.
   - They can be either functional components or class components.
   - Functional components are simple functions that return JSX.
   - Class components are ES6 classes that extend React.Component and have a render method.

3. **JSX (JavaScript XML):**
   - JSX is a syntax extension for JavaScript that allows us to write HTML-like code within JavaScript.
   - It makes React code more readable and easier to write.

4. **State and Props:**
   - State is an object that represents the parts of a component that can change over time.
   - Props (short for properties) are inputs to a React component.
   - State is managed internally by the component, while props are passed from parent to child components.

5. **Lifecycle Methods:**
   - Lifecycle methods are special methods that are automatically invoked at various stages in the life cycle of a React component.
   - They allow us to perform actions such as initializing state, fetching data, and updating the DOM in response to changes.

6. **Handling Events:**
   - React uses synthetic events to handle DOM events in a cross-browser-compatible way.
   - Event handlers in React are written in camelCase, e.g., onClick instead of onclick.

7. **Hooks:**
   - Hooks are functions that let us use state and other React features without writing a class.
   - They were introduced in React 16.8 to allow functional components to have state and lifecycle methods.

8. **Notes:**
   - Make sure to break down the UI into reusable components for better maintainability.
   - Practice using state and props effectively to manage data flow within components.
   - Experiment with different lifecycle methods to understand when they are invoked and how they can be used.
   - Explore the latest features and best practices in React, such as hooks and context API.

Overall, React provides a powerful and efficient way to build dynamic and interactive user interfaces, and mastering its core concepts is essential for becoming a proficient in react.


---

## Introduction to React

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

### JSX 

JSX (JavaScript XML) is a syntax extension for JavaScript that allows you to write HTML-like code directly within your JavaScript files. It's not mandatory to use JSX in React, but it's a common and recommended practice because it makes your code more readable and expressive.

#### Example:

```jsx
// JSX syntax example
const element = <h1>Hello, World!</h1>;

// Transpiles to JavaScript
const element = React.createElement('h1', null, 'Hello, World!');
```

In the JSX example, `<h1>Hello, World!</h1>` looks like HTML, but it's actually JSX. When React encounters JSX, it transforms it into regular JavaScript using `React.createElement()`. The resulting JavaScript code creates a React element representing the `<h1>` with the text "Hello, World!".

Absolutely! Let's break down JSX Syntax into simple steps with examples:

#### Step 1: What is JSX?

JSX stands for JavaScript XML. It's a syntax extension for JavaScript that allows you to write HTML-like code directly within your JavaScript files. JSX makes it easier to describe what the UI should look like in React applications.

#### Step 2: How does JSX work?

In JSX, you can write HTML-like syntax within curly braces `{}`. This syntax gets transformed into regular JavaScript code using a transpiler like Babel before it's interpreted by the browser.

#### Step 3: Understanding JSX Elements

In JSX, you can create elements similar to HTML elements. For example:

```jsx
const element = <h1>Hello, World!</h1>;
```

In this example, `<h1>Hello, World!</h1>` is a JSX element representing a heading with the text "Hello, World!". This JSX syntax is transformed into regular JavaScript code by React behind the scenes.

#### Step 4: Embedding JavaScript Expressions in JSX

You can embed JavaScript expressions within curly braces `{}` in JSX. For example:

```jsx
const name = 'John';
const element = <h1>Hello, {name}!</h1>;
```

In this example, `{name}` is a JavaScript expression that gets evaluated and inserted into the JSX element. The resulting element would be `<h1>Hello, John!</h1>`.

#### Step 5: JSX Attributes

In JSX, you can also specify HTML attributes just like you would in HTML. For example:

```jsx
const element = <a href="https://www.example.com">Click here</a>;
```

In this example, `href="https://www.example.com"` is an attribute of the `<a>` element.

#### Step 6: JSX and JavaScript Objects

JSX can also accept JavaScript objects as attributes. For example:

```jsx
const attrs = {
  className: 'btn',
  onClick: handleClick
};

const button = <button {...attrs}>Click me</button>;
```

In this example, `...attrs` spreads the properties of the `attrs` object as attributes of the `<button>` element.

#### Example:

Putting it all together:

```jsx
const name = 'John';
const element = (
  <div>
    <h1>Hello, {name}!</h1>
    <p>Welcome to our website.</p>
  </div>
);
```

In this example, `element` is a JSX element representing a `<div>` containing an `<h1>` heading with the text "Hello, John!" and a `<p>` paragraph with the text "Welcome to our website.".

#### Summary:

- JSX is a syntax extension for JavaScript that allows you to write HTML-like code within your JavaScript files.
- JSX elements are transformed into regular JavaScript code before being interpreted by the browser.
- You can embed JavaScript expressions and use HTML attributes in JSX.
- JSX makes it easier to describe the UI in React applications.

---

## Creating and Rendering React Components

In React, components are reusable, self-contained building blocks for your UI. There are two main types of components: functional components and class components.

#### Functional Components:

Functional components are JavaScript functions that accept props as arguments and return JSX elements. They are simpler and more lightweight than class components, making them ideal for presentational components that don't need state or lifecycle methods.

#### Example:

```jsx
// Functional Component Example
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}

// Rendering the Component
ReactDOM.render(
  <Greeting name="John" />,
  document.getElementById('root')
);
```

In this example, `Greeting` is a functional component that accepts a `name` prop and returns an `<h1>` element with a greeting message.

#### Class Components:

Class components are ES6 classes that extend `React.Component`. They have additional features like state and lifecycle methods, making them suitable for more complex components that need to manage their own state or perform side effects.

#### Example:

```jsx
// Class Component Example
class Greeting extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}!</h1>;
  }
}
```

In this example, `Greeting` is a class component that also accepts a `name` prop and returns an `<h1>` element with a greeting message. The `render()` method is required in class components and returns the JSX to be rendered.

#### Mored Detailed Explanation

#### Step 1: Understanding React Components

In React, components are like custom HTML elements that you can create and use to build your UI. They encapsulate the UI logic and can be reused throughout your application.

#### Step 2: Functional Components

Functional components are JavaScript functions that accept props (properties) as arguments and return JSX (JavaScript XML) elements. They are the simplest type of component and are primarily used for presentational purposes.

#### Example:

```jsx
// Functional Component
function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}
```

#### Step 3: Rendering Components

Once you've defined a component, you can render it by including it in the JSX of another component or in the `ReactDOM.render()` method.

#### Example:

```jsx
// Rendering the Component
ReactDOM.render(
  <Greeting name="John" />,
  document.getElementById('root')
);
```

In this example, we're rendering the `Greeting` component and passing the `name` prop with the value `"John"`.

#### Step 4: Class Components

Class components are ES6 classes that extend `React.Component`. They have additional features like state and lifecycle methods, making them suitable for more complex components.

#### Example:

```jsx
// Class Component
class Greeting extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}!</h1>;
  }
}
```

#### Step 5: Behind the Scenes - Component Rendering

When a component is rendered, React calls its `render()` method to generate the JSX representation of the component. This JSX is then transformed into a React element, which is ultimately rendered to the DOM.

#### Step 6: Props and State

Props are read-only properties passed to a component from its parent. They allow you to pass data from one component to another. State, on the other hand, is mutable and managed internally by the component. It represents the component's internal state and can be changed over time.

#### Step 7: Functional Components vs. Class Components

Functional components are simpler and primarily used for presentational purposes, while class components are more powerful and used for complex components that require state or lifecycle methods.

#### Summary:

- React components are like custom HTML elements used to build the UI.
- Functional components are simple JavaScript functions that return JSX elements.
- Class components are ES6 classes that extend `React.Component` and have additional features like state and lifecycle methods.
- Components are rendered by including them in the JSX of another component or using `ReactDOM.render()`.


---

###  Props and State in React

#### Step 1: Understanding Props

Props (short for properties) are a way to pass data from a parent component to a child component in React. They allow you to customize and configure a component's behavior and appearance.

#### Example:

```jsx
// Parent Component
function ParentComponent() {
  return <ChildComponent name="John" />;
}

// Child Component
function ChildComponent(props) {
  return <p>Hello, {props.name}!</p>;
}
```

In this example, the `ParentComponent` passes the `name` prop with the value `"John"` to the `ChildComponent`.

#### Step 2: Passing Data with Props

Props are passed as attributes in JSX when you render a component. The child component can access props through its function arguments.

#### Step 3: Understanding State

State represents the data that a component manages internally. It allows components to keep track of changing data and re-render when the state updates.

#### Example:

```jsx
// Class Component with State
class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  render() {
    return (
      <div>
        <p>Count: {this.state.count}</p>
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>
          Increment
        </button>
      </div>
    );
  }
}
```

In this example, the `Counter` component manages its internal state with a `count` variable.

#### Step 4: Managing State with Hooks

In functional components, you can manage state using the `useState` hook provided by React. This hook allows you to add state to functional components without needing to use classes.

#### Example:

```jsx
// Functional Component with State using useState Hook
function Counter() {
  const [count, setCount] = React.useState(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```

#### Step 5: Behind the Scenes - State Management

Behind the scenes, React uses a reconciliation algorithm to efficiently update the UI when state changes. React compares the previous state with the new state to determine what parts of the UI need to be updated.

#### Step 6: Updating State

State can be updated using the `setState` method in class components or the setter function returned by the `useState` hook in functional components. When state is updated, React automatically re-renders the component to reflect the changes.

#### Summary:

- Props allow you to pass data from parent to child components.
- State represents the internal data managed by a component.
- Class components use the `setState` method to manage state, while functional components use the `useState` hook.
- React efficiently updates the UI when state changes using a reconciliation algorithm.


---

### Handling Events in React

#### Step 1: Understanding Event Handling

In React, event handling allows you to capture and respond to user interactions, such as clicks, mouse movements, and keyboard inputs. Event handlers are functions that are called when a specific event occurs.

#### Step 2: Adding Event Handlers to Components

You can add event handlers to components by passing them as props. When the event occurs, React calls the corresponding event handler function.

#### Example:

```jsx
// Functional Component with Event Handling
function Button() {
  const handleClick = () => {
    alert('Button clicked!');
  };

  return <button onClick={handleClick}>Click me</button>;
}
```

In this example, the `handleClick` function is called when the button is clicked.

#### Step 3: Understanding the Event Object

In React, event handlers receive an event object as an argument. This object contains information about the event, such as the type of event, the target element, and any additional data associated with the event.

#### Step 4: Updating State Based on User Interactions

You can update component state based on user interactions by calling the `setState` method or using the `useState` hook. This allows you to dynamically change the UI in response to user actions.

#### Example:

```jsx
// Functional Component with State and Event Handling
function Counter() {
  const [count, setCount] = React.useState(0);

  const handleIncrement = () => {
    setCount(count + 1);
  };

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={handleIncrement}>Increment</button>
    </div>
  );
}
```

In this example, clicking the button increments the `count` state.

### Step 5: Behind the Scenes - Event Handling

Behind the scenes, React uses event delegation to handle events efficiently. When an event occurs, React captures it at the root of the component tree and delegates it to the appropriate component.

### Summary:

- Event handling in React allows you to capture and respond to user interactions.
- Event handlers are functions that are called when a specific event occurs.
- Event handlers receive an event object as an argument, which contains information about the event.
- You can update component state based on user interactions to dynamically change the UI.
- React uses event delegation to handle events efficiently.

---
Certainly! Let's explore the topic of rendering lists and using keys in React, covering everything from the basics to more advanced concepts, including behind-the-scenes explanations.

### Lists and Keys in React

#### Step 1: Rendering Lists of Data with the `map` Method

In React, you can render lists of data by using the `map` method on arrays. This allows you to generate UI elements dynamically based on the items in the array.

#### Example:

```jsx
function TodoList({ todos }) {
  return (
    <ul>
      {todos.map(todo => (
        <li key={todo.id}>{todo.text}</li>
      ))}
    </ul>
  );
}
```

In this example, the `TodoList` component receives an array of `todos` as a prop. It uses the `map` method to iterate over the `todos` array and generate a list item (`<li>`) for each todo item.

#### Step 2: Using the `key` Prop to Optimize List Rendering

When rendering lists in React, it's important to provide a unique `key` prop to each dynamically generated element. This helps React identify which elements have changed, added, or removed, improving performance and avoiding potential rendering issues.

#### Example:

```jsx
function TodoList({ todos }) {
  return (
    <ul>
      {todos.map(todo => (
        <li key={todo.id}>{todo.text}</li>
      ))}
    </ul>
  );
}
```

In this example, each todo item has a unique `id` that serves as the `key` prop for the corresponding list item.

#### Step 3: Handling Dynamic Data Rendering

When dealing with dynamic data, such as data fetched from an API or received from a parent component, you can pass the data as props to child components and render it dynamically using the `map` method.

#### Example:

```jsx
function ParentComponent() {
  const todos = [
    { id: 1, text: 'Learn React' },
    { id: 2, text: 'Build a project' },
    { id: 3, text: 'Deploy to production' }
  ];

  return <TodoList todos={todos} />;
}
```

In this example, the `ParentComponent` passes an array of `todos` as a prop to the `TodoList` component, which then renders the list dynamically using the `map` method.

#### Step 4: Behind the Scenes - List Rendering Optimization

When React renders a list of elements, it uses the `key` prop to efficiently update the DOM. React compares the `key` prop of each element in the new list with the corresponding element in the previous list to determine which elements need to be added, removed, or updated.

#### Summary:

- Rendering lists of data in React is done using the `map` method on arrays.
- Providing a unique `key` prop to each dynamically generated element helps React optimize list rendering and avoid potential issues.
- Dynamic data can be passed as props to child components and rendered dynamically using the `map` method.
- Behind the scenes, React uses the `key` prop to efficiently update the DOM when rendering lists of elements.

---

### Conditional Rendering

**Step 1: Using Conditional Statements to Render Components Conditionally**

In React, you can use conditional statements such as `if`, `else`, and ternary operators (`? :`) to conditionally render components based on certain conditions.

**Example:**

```jsx
function Greeting({ isLoggedIn }) {
  if (isLoggedIn) {
    return <p>Welcome back!</p>;
  } else {
    return <p>Please log in.</p>;
  }
}
```

In this example, the `Greeting` component renders different messages based on the value of the `isLoggedIn` prop.

**Step 2: Toggling Component Visibility Based on State**

You can toggle the visibility of components based on component state. By updating the state, you can show or hide certain components in the UI.

**Example:**

```jsx
function ToggleComponent() {
  const [isVisible, setIsVisible] = useState(true);

  const toggleVisibility = () => {
    setIsVisible(!isVisible);
  };

  return (
    <div>
      <button onClick={toggleVisibility}>Toggle</button>
      {isVisible && <p>Visible content</p>}
    </div>
  );
}
```

In this example, clicking the "Toggle" button toggles the visibility of the `<p>` element based on the `isVisible` state.

**Step 3: Behind the Scenes - Conditional Rendering Optimization**

When conditionally rendering components in React, only the necessary components are included in the virtual DOM. React efficiently updates the DOM based on changes in component state or props, ensuring optimal performance.

**Summary:**

- Conditional rendering in React allows you to show or hide components based on certain conditions using conditional statements.
- Toggling component visibility based on state enables dynamic UI behavior where components can appear or disappear based on user interactions or other factors.
- React optimizes conditional rendering by only including necessary components in the virtual DOM, ensuring efficient updates and optimal performance.

---


### Forms and Controlled Components

**Step 1: Handling Form Inputs in React**

In React, form inputs such as text fields, checkboxes, and radio buttons are managed as controlled components. This means that the value of the input is controlled by React state.

**Example:**

```jsx
import React, { useState } from 'react';

function LoginForm() {
  const [username, setUsername] = useState('');
  const [password, setPassword] = useState('');

  const handleUsernameChange = (event) => {
    setUsername(event.target.value);
  };

  const handlePasswordChange = (event) => {
    setPassword(event.target.value);
  };

  const handleSubmit = (event) => {
    event.preventDefault();
    // Handle form submission here
  };

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="text"
        value={username}
        onChange={handleUsernameChange}
        placeholder="Username"
      />
      <input
        type="password"
        value={password}
        onChange={handlePasswordChange}
        placeholder="Password"
      />
      <button type="submit">Login</button>
    </form>
  );
}
```

In this example, the `LoginForm` component manages the state of the username and password inputs using the `useState` hook. Event handlers (`handleUsernameChange` and `handlePasswordChange`) update the state when the input values change.

**Step 2: Managing Form State with Controlled Components**

In React, form inputs are controlled components, meaning their value is controlled by React state. This allows React to have full control over the input values and enables features like validation and dynamic updates.

Example:

```jsx
function LoginForm() {
  const [formData, setFormData] = useState({ username: '', password: '' });

  const handleChange = (event) => {
    const { name, value } = event.target;
    setFormData({ ...formData, [name]: value });
  };

  const handleSubmit = (event) => {
    event.preventDefault();
    // Handle form submission with formData
  };

  return (
    <form onSubmit={handleSubmit}>
      <input
        type="text"
        name="username"
        value={formData.username}
        onChange={handleChange}
        placeholder="Username"
      />
      <input
        type="password"
        name="password"
        value={formData.password}
        onChange={handleChange}
        placeholder="Password"
      />
      <button type="submit">Login</button>
    </form>
  );
}
```

In this example, the form data is managed as an object in state (`formData`). The `handleChange` function updates the corresponding property in `formData` whenever an input value changes.

**Step 3: Form Submission and Validation**

React provides various techniques for handling form submission and validation, including preventing default behavior (`event.preventDefault()`), client-side validation using state and conditions, and library solutions like Formik and Yup for more complex scenarios.

**Step 4: Behind the Scenes - Controlled Components**

Behind the scenes, React tracks the state of each controlled component and updates the UI accordingly. When an input value changes, React re-renders the component with the updated value, ensuring a consistent and controlled user experience.

**Summary:**

- Forms in React are managed as controlled components, where input values are controlled by React state.
- Managing form state allows for features like validation, dynamic updates, and controlled behavior.
- React provides various techniques for form submission and validation, including event handling, state management, and library solutions.
- Controlled components in React ensure a consistent and controlled user experience by tracking input values and updating the UI accordingly.

---

### Lifecycle Methods in Class Components

Step 1: Understanding Lifecycle Methods in Class Components

In React class components, lifecycle methods are special methods that are automatically invoked at various stages of a component's lifecycle. These methods allow you to perform certain actions or operations at specific points during the component's existence.

Example:

```jsx
import React, { Component } from 'react';

class MyComponent extends Component {
  constructor(props) {
    super(props);
    // Constructor: Initialize state and bind methods
  }

  componentDidMount() {
    // componentDidMount: Called after the component is mounted (added to the DOM)
    // Perform actions like fetching data from an API
  }

  componentDidUpdate(prevProps, prevState) {
    // componentDidUpdate: Called after the component's state or props are updated
    // Perform actions based on state/props changes
  }

  componentWillUnmount() {
    // componentWillUnmount: Called just before the component is unmounted and destroyed
    // Clean up tasks like removing event listeners or subscriptions
  }

  render() {
    // Render method: Return the component's UI
    return (
      <div>
        {/* Component UI */}
      </div>
    );
  }
}
```

In this example, we have defined several lifecycle methods within a class component. Each method serves a specific purpose and is invoked automatically by React at different stages of the component's lifecycle.

Step 2: Component Lifecycle Phases: Mounting, Updating, and Unmounting

React class components go through three main lifecycle phases: Mounting, Updating, and Unmounting.

- **Mounting**: Occurs when the component is first created and added to the DOM.
  - `constructor`: Initializes state and binds methods.
  - `componentDidMount`: Invoked after the component is mounted. Ideal for performing tasks like data fetching.

- **Updating**: Occurs when the component's state or props change.
  - `componentDidUpdate`: Invoked after the component's state or props are updated. Useful for responding to changes and performing side effects.

- **Unmounting**: Occurs when the component is removed from the DOM.
  - `componentWillUnmount`: Invoked just before the component is unmounted and destroyed. Used for cleanup tasks like removing event listeners or subscriptions.

Step 3: Behind the Scenes - Lifecycle Methods Execution

Behind the scenes, React manages the execution of lifecycle methods to ensure proper initialization, updating, and cleanup of components. These methods provide developers with hooks to perform tasks at specific points in the component's lifecycle, enabling better control and management of application behavior.

Summary:

- Lifecycle methods in React class components allow you to perform actions at specific stages of the component's lifecycle.
- The three main phases of the component lifecycle are Mounting, Updating, and Unmounting.
- Lifecycle methods like `componentDidMount`, `componentDidUpdate`, and `componentWillUnmount` provide hooks for performing tasks such as data fetching, responding to state changes, and cleanup.
- React manages the execution of lifecycle methods behind the scenes to ensure proper initialization, updating, and cleanup of components.

[Top](#table-of-contents)

---


###  Hooks

**Step 1: Understanding Hooks**

React Hooks are functions that allow functional components to use state, lifecycle methods, and other React features without writing a class. They were introduced in React 16.8 to address certain limitations and complexities associated with class components.

Example:

```jsx
import React, { useState, useEffect } from 'react';

function MyComponent() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    document.title = `You clicked ${count} times`;
  }, [count]);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

In this example, the `useState` and `useEffect` hooks are used within a functional component to manage state and perform side effects respectively.

**Step 2: Why We Need Hooks**

1. **Simplify State Management**: Hooks simplify state management by allowing functional components to have local state.
2. **Reusability**: Hooks promote code reuse by allowing logic to be encapsulated and reused across components.
3. **Avoid Class Boilerplate**: Hooks eliminate the need for class components and the associated boilerplate code.
4. **Enhanced Readability**: Hooks make code more readable and maintainable by organizing logic in a more concise manner.

**Step 3: Advantages of Hooks**

1. **Easier to Understand**: Hooks make it easier to understand and reason about the behavior of a component.
2. **Separation of Concerns**: Hooks encourage separation of concerns by allowing logic to be decoupled from UI rendering.
3. **Improved Performance**: Hooks can lead to better performance optimizations compared to class components in certain scenarios.
4. **Support for Functional Components**: Hooks enable functional components to have state and lifecycle features previously exclusive to class components.

**Step 4: Problems Hooks Solve**

1. **Complexity of Class Components**: Hooks address the complexity associated with class components, such as the use of `this` keyword and lifecycle methods.
2. **Code Duplication**: Hooks reduce code duplication by enabling logic to be shared across multiple components.
3. **Difficulty in Testing**: Hooks make testing easier by allowing logic to be tested independently of the component's rendering.

**Step 5: Disadvantages of Hooks**

1. **Learning Curve**: Hooks introduce a new way of writing components, which may have a learning curve for developers accustomed to class components.
2. **Breaking Changes**: Introducing hooks may require significant changes to existing class components, leading to potential breaking changes.
3. **Tooling Support**: Some IDEs and development tools may not provide full support for hooks, leading to limitations in tooling features.

**Step 6: Difference from Lifecycle Methods in Class Components**

Hooks differ from lifecycle methods in class components in several ways:
- **No `this` Context**: Hooks do not rely on `this` context, making it easier to use and understand.
- **No Need for Class Syntax**: Hooks allow functional components to access state and lifecycle features without using class syntax.
- **Granular Control**: Hooks provide granular control over state and side effects, allowing for more flexibility and composability.

**Step 7: Behind the Scenes - How Hooks Work**

Behind the scenes, React manages the state and lifecycle of components using hooks by maintaining a queue of updates and ensuring they are applied in the correct order. Hooks allow React to track dependencies and schedule updates efficiently, resulting in optimal performance.

**Here's a list of important React hooks that every React programmer should know:**

1. **useState**: Allows functional components to manage state.
2. **useEffect**: Enables performing side effects in functional components, such as data fetching or DOM manipulation.
3. **useContext**: Provides access to the React context API within functional components.
4. **useReducer**: Alternative to `useState` for managing more complex state logic.
5. **useCallback**: Memoizes functions to prevent unnecessary re-renders in functional components.
6. **useMemo**: Memoizes values to optimize performance in functional components.
7. **useRef**: Provides access to the DOM node or a mutable value within functional components.
8. **useLayoutEffect**: Similar to `useEffect`, but fires synchronously after all DOM mutations.
9. **useImperativeHandle**: Allows components to customize the instance value that is exposed to parent components when using `forwardRef`.
10. **useDebugValue**: Adds a label to custom hooks for easier debugging in React DevTools.

These are some of the most commonly used React hooks that cover a wide range of functionalities. Familiarizing yourself with these hooks will enable you to build robust and efficient React applications.

**Summary:**

- React Hooks provide a more flexible and concise way to manage state and side effects in functional components.
- They address the limitations and complexities associated with class components, leading to improved code readability and maintainability.
- While hooks offer numerous advantages, they may also have a learning curve and require adjustments to existing codebases.
- Understanding how hooks work behind the scenes can help developers leverage their power effectively while building React applications.

[Top](#table-of-contents)

---


### useState 

Step 1: Understanding useState

The `useState` hook is a built-in React hook that allows functional components to manage state. It enables components to have stateful behavior, similar to class components.

Example:

```jsx
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```

In this example, `useState` is used to create a piece of state named `count`, initialized with a value of `0`. The `setCount` function is used to update the state.

Step 2: Why We Need useState

1. **State Management**: `useState` simplifies state management in functional components, allowing them to have stateful behavior without using class components.
2. **Avoiding Class Components**: With `useState`, there's no need to use class components solely for managing state, reducing boilerplate code and complexity.
3. **Functional Style**: Using hooks promotes a functional programming style, making components more predictable and easier to reason about.

Step 3: Advantages of useState

1. **Simplicity**: `useState` is easy to understand and use, making state management straightforward in functional components.
2. **Flexibility**: It allows components to have local state, enabling them to respond to user interactions and update the UI dynamically.
3. **Performance**: `useState` is optimized for performance and efficiently updates the component state when needed.

Step 4: Problems useState Solves

1. **Stateful Behavior**: `useState` enables functional components to have stateful behavior, solving the problem of components being stateless by default.
2. **Data Persistence**: It ensures that component state persists across re-renders, allowing components to maintain their state between updates.

Step 5: Disadvantages of useState

1. **Complex State Logic**: For complex state logic, managing state with `useState` alone might become cumbersome. In such cases, `useReducer` or custom hooks may be more appropriate.
2. **Limited to Functional Components**: `useState` is only available in functional components, so it cannot be used in class components.

Step 6: Behind the Scenes - How useState Works

Behind the scenes, React maintains the state created by `useState` and ensures that updates to the state trigger re-renders of the component. React's reconciliation process efficiently updates the DOM to reflect the changes in state.

Summary:

- `useState` is a built-in React hook used for managing state in functional components.
- It simplifies state management, making components more predictable and easier to understand.
- `useState` provides a flexible and efficient way to add stateful behavior to functional components, improving the overall development experience.

[Top](#table-of-contents)

---

### useEffect Hook

Step 1: Introduction to useEffect

The `useEffect` hook is a built-in React hook that allows functional components to perform side effects. Side effects may include data fetching, DOM manipulation, or subscribing to external data sources.

**Example:**

```jsx
import React, { useState, useEffect } from 'react';

function UserProfile({ userId }) {
  const [user, setUser] = useState(null);

  useEffect(() => {
    // Fetch user data from API
    fetch(`https://api.example.com/users/${userId}`)
      .then(response => response.json())
      .then(data => setUser(data));
  }, [userId]);

  return (
    <div>
      <h2>User Profile</h2>
      {user ? (
        <div>
          <p>Name: {user.name}</p>
          <p>Email: {user.email}</p>
        </div>
      ) : (
        <p>Loading...</p>
      )}
    </div>
  );
}
```

In this example, `useEffect` is used to fetch user data from an API when the `userId` prop changes.

Step 2: Why We Need useEffect

1. **Managing Side Effects**: `useEffect` allows functional components to perform side effects like data fetching, subscriptions, or DOM updates.
2. **Avoiding Class Components**: With `useEffect`, side effects can be managed in functional components, eliminating the need for class components solely for side effects.
3. **Asynchronous Behavior**: It enables asynchronous behavior within functional components, making it easier to work with asynchronous operations like fetching data.

Step 3: Advantages of useEffect

1. **Flexibility**: `useEffect` provides a flexible way to manage side effects, allowing components to respond to changes in state or props.
2. **Separation of Concerns**: It encourages separation of concerns by keeping side effects separate from the component's rendering logic.
3. **Efficiency**: `useEffect` is optimized for performance and ensures that side effects are executed in the correct order, avoiding race conditions and unexpected behavior.

Step 4: Problems useEffect Solves

1. **Managing Asynchronous Operations**: `useEffect` simplifies the management of asynchronous operations like data fetching, ensuring that side effects are executed at the appropriate times.
2. **Updating the UI**: It allows components to update the UI in response to changes in state or props, ensuring that the UI reflects the latest data.

Step 5: Disadvantages of useEffect

1. **Complexity**: Managing multiple side effects within a single `useEffect` hook or dealing with dependencies can sometimes lead to complex code.
2. **Debugging**: Debugging components with complex side effects may be challenging, especially when dealing with asynchronous behavior or race conditions.

Step 6: Behind the Scenes - How useEffect Works

Behind the scenes, React schedules side effects defined in `useEffect` to run after the component has been rendered to the DOM. React ensures that side effects are executed in the correct order and cleans them up when the component is unmounted or re-rendered.

Summary:

- `useEffect` is a built-in React hook used for managing side effects in functional components.
- It provides a flexible and efficient way to perform asynchronous operations, data fetching, and other side effects.
- `useEffect` promotes separation of concerns by keeping side effects separate from the component's rendering logic, improving code maintainability and readability.


[Top](#table-of-contents)

---


### Context and useContext Hook

**Step 1: Introduction to React Context API**

The React Context API provides a way to pass data through the component tree without having to pass props manually at every level. It's designed to share data that can be considered "global" for a tree of React components.

**Example:**

```jsx
// Creating a context
const ThemeContext = React.createContext('light');

// Providing a context value
<ThemeContext.Provider value="dark">
  <App />
</ThemeContext.Provider>

// Consuming a context value
<ThemeContext.Consumer>
  {theme => <Header theme={theme} />}
</ThemeContext.Consumer>
```

**Step 2: Creating and Consuming Contexts**

To create a context, use `React.createContext()`. Then, use `Provider` to pass a value to the context. Consumers can access this value anywhere in the component tree.

**Step 3: Using useContext Hook**

The `useContext` hook is a built-in React hook that allows functional components to consume context values. It provides a more concise way to access context values compared to the `Consumer` component.

**Example:**

```jsx
import React, { useContext } from 'react';

// Create a context
const ThemeContext = React.createContext('light');

// Functional component consuming context
function Header() {
  const theme = useContext(ThemeContext);
  return <header style={{ background: theme }}>Header</header>;
}
```

**Step 4: Why We Need Context and useContext**

1. **Avoiding Prop Drilling**: Context and `useContext` help avoid prop drilling, where props are passed down multiple levels of nested components.
2. **Global Data Sharing**: They enable sharing data across multiple components without the need to pass props manually at each level.
3. **Simplifying Component Composition**: Context and `useContext` make it easier to compose components and manage shared data in complex component hierarchies.

**Step 5: Advantages of Context and useContext**

1. **Simplicity**: Context and `useContext` simplify data sharing between components, reducing the complexity of passing props down the component tree.
2. **Flexibility**: They provide a flexible way to manage shared data, allowing components to access context values wherever they are in the component tree.
3. **Improved Performance**: Context and `useContext` can improve performance by eliminating unnecessary prop drilling and reducing the number of re-renders caused by prop changes.

**Step 6: Problems Context and useContext Solve**

1. **Prop Drilling**: They solve the problem of prop drilling by providing a way to access context values without passing props through intermediary components.
2. **Global State Management**: Context and `useContext` solve the problem of managing global state by providing a centralized mechanism for sharing data across components.

**Step 7: Disadvantages of Context and useContext**

1. **Complexity**: Context and `useContext` may introduce complexity, especially in large applications with multiple contexts and consumers.
2. **Overuse**: Using context for all data sharing needs may lead to overuse and make it harder to track data flow within the application.

**Step 8: Behind the Scenes - How Context and useContext Work**

Behind the scenes, React manages the propagation of context values and ensures that consumers are updated when the context value changes. This involves creating a context tree that mirrors the component tree and updating consumers when context values are updated.

**Summary:**

- React Context API and the `useContext` hook provide a way to share data across components without prop drilling.
- They simplify data sharing and improve component composition by allowing components to access context values anywhere in the component tree.
- Context and `useContext` offer advantages such as simplicity, flexibility, and improved performance, but they may introduce complexity and should be used judiciously.


[Top](#table-of-contents)

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






  
