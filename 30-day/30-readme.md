# 01-June-2022- 30th class reading notes:


## Redux - Asynchronous Actions

### Redux Middleware and Side Effects

By itself, a Redux store doesn't know anything about async logic. It only knows how to synchronously dispatch actions, update the state by calling the root reducer function, and notify the UI that something has changed. Any asynchronicity has to happen outside the store.

Earlier, we said that Redux reducers must never contain "side effects". A "side effect" is any change to state or behavior that can be seen outside of returning a value from a function. Some common kinds of side effects are things like:

- Logging a value to the console
- Saving a file
- Setting an async timer
- Making an AJAX HTTP request
- Modifying some state that exists outside of a function, or mutating arguments to a function
- Generating random numbers or unique random IDs (such as Math.random() or Date.now())

**Redux middleware were designed to enable writing logic that has side effects.**

a Redux middleware can do anything when it sees a dispatched action: log something, modify the action, delay the action, make an async call, and more. Also, since middleware form a pipeline around the real store.dispatch function, this also means that we could actually pass something that isn't a plain action object to dispatch, as long as a middleware intercepts that value and doesn't let it reach the reducers.

Middleware also have access to dispatch and getState. That means you could write some async logic in a middleware, and still have the ability to interact with the Redux store by dispatching actions.

### Writing an Async Function Middleware

Both of the middleware in that last section were very specific and only do one thing. It would be nice if we had a way to write any async logic ahead of time, separate from the middleware itself, and still have access to dispatch and getState so that we can interact with the store.

What if we wrote a middleware that let us pass a function to dispatch, instead of an action object? We could have our middleware check to see if the "action" is actually a function instead, and if it's a function, call the function right away. That would let us write async logic in separate functions, outside of the middleware definition.

### Redux Async Data Flow

So how do middleware and async logic affect the overall data flow of a Redux app?

Just like with a normal action, we first need to handle a user event in the application, such as a click on a button. Then, we call dispatch(), and pass in something, whether it be a plain action object, a function, or some other value that a middleware can look for.

Once that dispatched value reaches a middleware, it can make an async call, and then dispatch a real action object when the async call completes.

Earlier, we saw a diagram that represents the normal synchronous Redux data flow. When we add async logic to a Redux app, we add an extra step where middleware can run logic like AJAX requests, then dispatch actions.

![redux](./redux.gif)

### Using the Redux Thunk Middleware

As it turns out, Redux already has an official version of that "async function middleware", called the Redux "Thunk" middleware. The thunk middleware allows us to write functions that get dispatch and getState as arguments. The thunk functions can have any async logic we want inside, and that logic can dispatch actions and read the store state as needed.

Writing async logic as thunk functions allows us to reuse that logic without knowing what Redux store we're using ahead of time.

### Fetching Todos from a Server

Right now our todo entries can only exist in the client's browser. We need a way to load a list of todos from the server when the app starts up.

We'll start by writing a thunk function that makes an AJAX call to our /fakeApi/todos endpoint to request an array of todo objects, and then dispatch an action containing that array as the payload.


[Redux Thunk](https://github.com/reduxjs/redux-thunk)


[gh-pages](https://marah-jaradat.github.io/advanced-js-reading-notes/)

[My-repo](https://github.com/marah-jaradat/advanced-js-reading-notes/blob/gh-pages/30-day/30-readme.md)