# 24-April-2022- 17th class reading notes:

## Component Based UI:

### **Introducing JSX**

React embraces the fact that rendering logic is inherently coupled with other UI logic: how events are handled, how the state changes over time, and how the data is prepared for display.

Instead of artificially separating technologies by putting markup and logic in separate files, React separates concerns with loosely coupled units called “components” that contain both. We will come back to components in a further section, but if you’re not yet comfortable putting markup in JS, this talk might convince you otherwise.

Specifying Attributes with JSX
- You may use quotes to specify string literals as attributes
- You may also use curly braces to embed a JavaScript expression in an attribute
- Don’t put quotes around curly braces when embedding a JavaScript expression in an attribute. You should either use quotes (for string values) or curly braces (for expressions), but not both in the same attribute.
  
**Warning:**
Since JSX is closer to JavaScript than to HTML, React DOM uses camelCase property naming convention instead of HTML attribute names.
For example, class becomes className in JSX, and tabindex becomes tabIndex.

### **Rendering Elements**

An element describes what you want to see on the screen.
Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.

Applications built with just React usually have a single root DOM node. If you are integrating React into an existing app, you may have as many isolated root DOM nodes as you like.
To render a React element, first pass the DOM element to ReactDOM.createRoot(), then pass the React element to root.render()


### **Components and Props**

Components let you split the UI into independent, reusable pieces, and think about each piece in isolation. This page provides an introduction to the idea of components. You can find a detailed component API reference here.

Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.
 [react components](https://reactjs.org/docs/react-component.html)

**Function and Class Components**
The simplest way to define a component is to write a JavaScript function
Function is a valid React component because it accepts a single “props” (which stands for properties) object argument with data and returns a React element. We call such components “function components” because they are literally JavaScript functions.

Note: Always start component names with a capital letter.
React treats components starting with lowercase letters as DOM tags. For example, <div /> represents an HTML div tag, but <Welcome /> represents a component and requires Welcome to be in scope.
To learn more about the reasoning behind this convention, please read JSX In Depth.


[cheat sheet](https://devhints.io/sass)