# 28-May-2022- 28th class reading notes:


## Application State with Redux

### Redux

A Predictable State Container for JS Apps
It helps you write applications that behave consistently, run in different environments (client, server, and native), and are easy to test. On top of that, it provides a great developer experience, such as live code editing combined with a time traveling debugger.

You can use Redux together with React, or with any other view library. It is tiny (2kB, including dependencies), but has a large ecosystem of addons available.

### Installation
#### Redux Toolkit
Redux Toolkit is our official recommended approach for writing Redux logic. It wraps around the Redux core, and contains packages and functions that we think are essential for building a Redux app. Redux Toolkit builds in our suggested best practices, simplifies most Redux tasks, prevents common mistakes, and makes it easier to write Redux applications.

RTK includes utilities that help simplify many common use cases, including store setup, creating reducers and writing immutable update logic, and even creating entire "slices" of state at once.

Whether you're a brand new Redux user setting up your first project, or an experienced user who wants to simplify an existing application, Redux Toolkit can help you make your Redux code better.

#### Create a React Redux App
The recommended way to start new apps with React and Redux is by using the official Redux+JS template or Redux+TS template for Create React App, which takes advantage of Redux Toolkit and React Redux's integration with React components.

#### Redux Core
The Redux core library is available as a package on NPM for use with a module bundler or in a Node application:
It is also available as a precompiled UMD package that defines a window.Redux global variable. The UMD package can be used as a script directly.


[fundamentals](https://app.egghead.io/playlists/fundamentals-of-redux-course-from-dan-abramov-bd5cc867)

[presentation-reactathon](https://blog.isquaredsoftware.com/2018/03/presentation-reactathon-redux-fundamentals/)

[redux-tutorial](https://daveceddia.com/redux-tutorial/)

### Testing redux reducers with Jest

#### Reducers

Just a quick refresher on what reducer is before we go into testing and code. Redux documentation is still great, in fact it covers unit tests really well you don’t even have to read this post. To summarize it, the reducer is a pure function that takes the previous state and an action, and returns the next state.

#### Pure functions

Because it’s a pure function, it’s easy to test. It’s a function that produces no side effects; given the same input, will always return the same output; doesn’t rely on external state.

[full-guide](https://www.freecodecamp.org/news/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6)


[gh-pages](https://marah-jaradat.github.io/advanced-js-reading-notes/)

[My-repo](https://github.com/marah-jaradat/advanced-js-reading-notes/blob/gh-pages/28th-day/28-readme.md)