# 📚 React Basics

React is one of the most popular libraries for building modern web applications.

## 1. What is React?
React is a **JavaScript Library** that helps build **interactive user interfaces** efficiently.  
It breaks the UI into reusable components, making development faster and easier.

**Why it matters:**  
React updates only the parts of the UI that change, improving performance and user experience.

---

## 2. What is JSX?
- **JSX = JavaScript XML**
- A syntax extension for JavaScript that looks like HTML but works inside React.
- Makes writing UI components easier by combining JavaScript and HTML-like markup.

**Example:**
```jsx
const element = <h1>Hello, React!</h1>;
```

---

## 3. What is Component? 
- A **Component** is a reusable, independent piece of UI.  
- It can be a **function** or a **class** that returns JSX.  
- Components must follow **PascalCase naming convention** (e.g., `MyComponent`).  

**Example:**
```jsx
function Welcome() {
  return <h2>Welcome to React!</h2>;
}

export default Welcome;
```

---

## 4. What is Fragment?
- A **Fragment** allows grouping multiple elements without adding extra DOM nodes (like an extra ```<div>```)
- Useful when you want to return multiple sibling elements

**Example:**
```jsx
function App(){
    return (  
        <>
            <h1> Hi </h1>
            <p> This is inside Fragment </p>
        </>
    );
}
``` 

---

## 5. What is Props?
- **Props** = **Properties**
- Used to **pass data from Parent to Child** components
- Props are **immutable** (read-only inside child components)

**Example:**
```jsx
function Greeting(props){
    return <p> Hello, {props.name}! </p>;
}

function App(){
    return (
        <div>
            <Greeting name = "Manideep" />
            <Greeting name = "React Learner" />
        </div>
    );
}
```

---

## 6. What is Guard Operator?
- The **Guard Operator(&&)** in React is used to **conditionally render** components
- If the condition is ```true```, the **JSX** after ```(&&)``` is displayed
- If the condition is ```false```, React ignores it (renders nothing).

**Example:**
```jsx
function App(){
    const isLoggedIn = true;

    return (
        <div>
            <h2> Hello! </h2>
            {isLoggedIn && <p> You are a logged in ✅</p>}
        </div>
    )
}
```