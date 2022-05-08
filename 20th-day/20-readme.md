# 08-May-2022- 20th class reading notes:

## Advanced State with Reducers:

### **useReducer**

 An alternative to useState. Accepts a reducer of type (state, action) => newState, and returns the current state paired with a dispatch method. (If you’re familiar with Redux, you already know how this works.)

useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one. useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.

 - Note

React guarantees that dispatch function identity is stable and won’t change on re-renders. This is why it’s safe to omit from the useEffect or useCallback dependency list.



**Specifying the initial state**
There are two different ways to initialize useReducer state. You may choose either one depending on the use case. The simplest way is to pass the initial state as a second argument:

const [state, dispatch] = useReducer(
    reducer,
    {count: initialCount}
  );

- Note

React doesn’t use the state = initialState argument convention popularized by Redux. The initial value sometimes needs to depend on props and so is specified from the Hook call instead. If you feel strongly about this, you can call useReducer(reducer, undefined, reducer) to emulate the Redux behavior, but it’s not encouraged.

**Lazy initialization**
You can also create the initial state lazily. To do this, you can pass an init function as the third argument. The initial state will be set to init(initialArg).

It lets you extract the logic for calculating the initial state outside the reducer. This is also handy for resetting the state later in response to an action

**Bailing out of a dispatch**
If you return the same value from a Reducer Hook as the current state, React will bail out without rendering the children or firing effects. (React uses the Object.is comparison algorithm.)

Note that React may still need to render that specific component again before bailing out. That shouldn’t be a concern because React won’t unnecessarily go “deeper” into the tree. If you’re doing expensive calculations while rendering, you can optimize them with useMemo.



## **useCallback**

const memoizedCallback = useCallback(
  () => {
    doSomething(a, b);
  },
  [a, b],
);

Returns a memoized callback.

Pass an inline callback and an array of dependencies. useCallback will return a memoized version of the callback that only changes if one of the dependencies has changed. This is useful when passing callbacks to optimized child components that rely on reference equality to prevent unnecessary renders (e.g. shouldComponentUpdate).

useCallback(fn, deps) is equivalent to useMemo(() => fn, deps).

**Note**

The array of dependencies is not passed as arguments to the callback. Conceptually, though, that’s what they represent: every value referenced inside the callback should also appear in the dependencies array. In the future, a sufficiently advanced compiler could create this array automatically.

We recommend using the exhaustive-deps rule as part of our eslint-plugin-react-hooks package. It warns when dependencies are specified incorrectly and suggests a fix.

### **useMemo**

const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);

Returns a memoized value.

Pass a “create” function and an array of dependencies. useMemo will only recompute the memoized value when one of the dependencies has changed. This optimization helps to avoid expensive calculations on every render.

Remember that the function passed to useMemo runs during rendering. Don’t do anything there that you wouldn’t normally do while rendering. For example, side effects belong in useEffect, not useMemo.

If no array is provided, a new value will be computed on every render.

You may rely on useMemo as a performance optimization, not as a semantic guarantee. In the future, React may choose to “forget” some previously memoized values and recalculate them on next render, e.g. to free memory for offscreen components. Write your code so that it still works without useMemo — and then add it to optimize performance.

### **useRef**

const refContainer = useRef(initialValue);

useRef returns a mutable ref object whose .current property is initialized to the passed argument (initialValue). The returned object will persist for the full lifetime of the component.
Keep in mind that useRef doesn’t notify you when its content changes. Mutating the .current property doesn’t cause a re-render. If you want to run some code when React attaches or detaches a ref to a DOM node, you may want to use a callback ref instead.

### **useImperativeHandle**

useImperativeHandle(ref, createHandle, [deps])
useImperativeHandle customizes the instance value that is exposed to parent components when using ref. As always, imperative code using refs should be avoided in most cases. 

## **Library Hooks**

The following Hooks are provided for library authors to integrate libraries deeply into the React model, and are not typically used in application code.

### **useSyncExternalStore**

const state = useSyncExternalStore(subscribe, getSnapshot[, getServerSnapshot]);

useSyncExternalStore is a hook recommended for reading and subscribing from external data sources in a way that’s compatible with concurrent rendering features like selective hydration and time slicing.

This method returns the value of the store and accepts three arguments:

- subscribe: function to register a callback that is called whenever the store changes.
- getSnapshot: function that returns the current value of the store.
- getServerSnapshot: function that returns the snapshot used during server rendering.

### **useInsertionEffect**

useInsertionEffect(didUpdate);

The signature is identical to useEffect, but it fires synchronously before all DOM mutations. Use this to inject styles into the DOM before reading layout in useLayoutEffect. Since this hook is limited in scope, this hook does not have access to refs and cannot schedule updates.

[Hooks API Reference](https://reactjs.org/docs/hooks-reference.html#usecallback)
[React useReducer](https://blog.logrocket.com/react-usereducer-hook-ultimate-guide/)