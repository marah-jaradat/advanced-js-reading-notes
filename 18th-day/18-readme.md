# 26-April-2022- 18th class reading notes:

## useState() Hook:

### **What is a Hook?**

 A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components. We’ll learn other Hooks later.

When would I use a Hook? If you write a function component and realize you need to add some state to it, previously you had to convert it to a class. Now you can use a Hook inside the existing function component. We’re going to do that right now!

### **Why Hooks?**

We know that components and top-down data flow help us organize a large UI into small, independent, reusable pieces. However, we often can’t break complex components down any further because the logic is stateful and can’t be extracted to a function or another component. Sometimes that’s what people mean when they say React doesn’t let them “separate concerns.”

These cases are very common and include animations, form handling, connecting to external data sources, and many other things we want to do from our components. When we try to solve these use cases with components alone, we usually end up with:

- Huge components that are hard to refactor and test.
- Duplicated logic between different components and lifecycle methods.
- Complex patterns like render props and higher-order components.

We think Hooks are our best shot at solving all of these problems. Hooks let us organize the logic inside a component into reusable isolated units

### **Do Hooks Make React Bloated?**

Before we look at Hooks in detail, you might be worried that we’re just adding more concepts to React with Hooks. That’s a fair criticism. I think that while there is definitely going to be a short-term cognitive cost to learning them, the end result will be the opposite.
If the React community embraces the Hooks proposal, it will reduce the number of concepts you need to juggle when writing React applications. Hooks let you always use functions instead of having to constantly switch between functions, classes, higher-order components, and render props.

### **What Are Hooks, Exactly?**

To understand Hooks, we need to take a step back and think about code reuse.
Today, there are a lot of ways to reuse logic in React apps. We can write simple functions and call them to calculate something. We can also write components (which themselves could be functions or classes). Components are more powerful, but they have to render some UI. This makes them inconvenient for sharing non-visual logic. This is how we end up with complex patterns like render props and higher-order components. Wouldn’t React be simpler if there was just one common way to reuse code instead of so many?

Functions seem to be a perfect mechanism for code reuse. Moving logic between functions takes the least amount of effort. However, functions can’t have local React state inside them. You can’t extract behavior like “watch window size and update the state” or “animate a value over time” from a class component without restructuring your code or introducing an abstraction like Observables. Both approaches hurt the simplicity that we like about React.

Hooks solve exactly that problem. Hooks let you use React features (like state) from a function — by doing a single function call. React provides a few built-in Hooks exposing the “building blocks” of React: state, lifecycle, and context.

Since Hooks are regular JavaScript functions, you can combine built-in Hooks provided by React into your own “custom Hooks”. 

### **So What About Classes?**

Custom Hooks are, in our opinion, the most appealing part of the Hooks proposal. But in order for custom Hooks to work, React needs to provide functions with a way to declare state and side effects. And that’s exactly what built-in Hooks like useState and useEffect let us do. You can learn about them in the documentation.

It turns out that these built-in Hooks aren’t only useful for creating custom Hooks. They are also sufficient for defining components in general, as they provide us with all the necessary features like state. This is why we’d like Hooks to become the primary way to define React components in the future.

We have no plans to deprecate classes. At Facebook we have tens of thousands of class components and, like you, we have no intention of rewriting them. But if the React community embraces Hooks, it doesn’t make sense to have two different recommended ways to write components. Hooks can cover all use cases for classes while providing more flexibility in extracting, testing, and reusing code. This is why Hooks represent our vision for the future of React.

[more](https://medium.com/@dan_abramov/making-sense-of-react-hooks-fdbde8803889)

**What does calling useState do?** It declares a “state variable”. Our variable is called count but we could call it anything else, like banana. This is a way to “preserve” some values between the function calls — useState is a new way to use the exact same capabilities that this.state provides in a class. Normally, variables “disappear” when the function exits but state variables are preserved by React.

**What do we pass to useState as an argument?** The only argument to the useState() Hook is the initial state. Unlike with classes, the state doesn’t have to be an object. We can keep a number or a string if that’s all we need. In our example, we just want a number for how many times the user clicked, so pass 0 as initial state for our variable. (If we wanted to store two different values in state, we would call useState() twice.)

**What does useState return?** It returns a pair of values: the current state and a function that updates it. This is why we write const [count, setCount] = useState(). This is similar to this.state.count and this.setState in a class, except you get them in a pair. If you’re not familiar with the syntax we used, we’ll come back to it at the bottom of this page.

[more hooks-state](https://reactjs.org/docs/hooks-state.html)
[more hooks-overview](https://reactjs.org/docs/hooks-overview.html)
[more Hooks-API-Reference](https://reactjs.org/docs/hooks-reference.html)
