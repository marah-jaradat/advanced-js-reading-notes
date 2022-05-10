# 10-May-2022:

## React: The Virtual DOM

A virtual DOM object is a representation of a DOM object, like a lightweight copy.
A virtual DOM object has the same properties as a real DOM object, but it lacks the real thing’s power to directly change what’s on the screen.

Manipulating the DOM is slow. Manipulating the virtual DOM is much faster, because nothing gets drawn onscreen. Think of manipulating the virtual DOM as editing a blueprint, as opposed to moving rooms in an actual house.

### How it helps

In summary, here’s what happens when you try to update the DOM in React:

- The entire virtual DOM gets updated.
- The virtual DOM gets compared to what it looked like before you updated it. React figures out which objects have changed.
- The changed objects, and the changed objects only, get updated on the real DOM.
- Changes on the real DOM cause the screen to change.

[Virtual DOM](https://www.codecademy.com/article/react-virtual-dom)


## Differences between Functional Components and Class Components in React

**Functional Components vs Class Components:**

|**Functional Components** | **Class Components** |
| --------------- | -------------------------------------- |
|A functional component is just a plain JavaScript function that accepts props as an argument and returns a React element.| A class component requires you to extend from React. Component and create a render function which returns a React element.|
|There is no render method used in functional components.|It must have the render() method returning JSX (which is syntactically similar to HTML)|
|Also known as Stateless components as they simply accept data and display them in some form, that they are mainly responsible for rendering UI.|Also known as Stateful components because they implement logic and state.|
|React lifecycle methods (for example, componentDidMount) cannot be used in functional components.|React lifecycle methods can be used inside class components (for example, componentDidMount).|
|Hooks can be easily used in functional components to make them Stateful. example: const [name,SetName]= React.useState(‘ ‘)|It requires different syntax inside a class component to implement hooks. example: constructor(props) {super(props);this.state = {name: ‘ ‘}}|
|Constructors are not used.|Constructor are used as it needs to store state. |

[Differences between Functional and Class Components](https://www.codecademy.com/article/react-virtual-dom)

## How to Deploy a Routed React App to GitHub Pages

When we build projects, we want to showcase them online. Instead of buying a domain and taking the time to configure it, it's easier just to host it using GitHub Pages.

A project that just uses JavaScript, HTML and CSS is simple to host on GitHub Pages. Projects that are built in React, Vue or Angular require some configurations, though. This gives anyone who visits your application online the same experience you have when you build the application locally.

**Prerequisites**

1. You need to have Node, yarn and npm installed on your machine. 

2. We will also need to create a repository on GitHub. Head over to your account and create a new repository. Choose whichever name you deem fit for this project, but I will go with starter-project for the rest of this article.

3. To create our project, we will be using create-react-app. It is a package that lets you create a single page application with ease. To create a project, you need to type the following in the terminal:
   npx create-react-app starter-project
   yarn start

**How to Deploy Your Project to GitHub**

You may have noticed that we have not created any repository in GitHub. So before we move on, we must have our project uploaded there. Head over to your GitHub account and create a repository with the same name as the React project.

We are going to add this repository as a remote to our project. To do that, in the terminal, type:
    git remote add <name-of-remote> <url-of-repository>
    git push --set-upstream origin master
    yarn add gh-pages

    npm run deploy

[gh-pages](https://www.freecodecamp.org/news/deploy-a-react-app-to-github-pages/)
[Netlify](https://www.netlify.com/github-pages-vs-netlify/)


## The Necessity of Bundlers and Transpilers Review Course

[Bundlers and Transpilers](https://www.udemy.com/tutorial/react-js-and-redux-mastering-web-apps/the-necessity-of-bundlers-and-transpilers-review/)

## React component lifecycle: React lifecycle methods & hooks

First, let’s take a look at how it’s been done traditionally. In order to do that, we’re going to take a closer look at React components.

As you probably know, each React component instance has a lifecycle. The component’s lifecycle consists of three phases:

1. Mounting lifecycle methods, that is inserting elements into the DOM.
    As we mentioned, during the mounting phase of the lifecycle, the class component is inserted into the DOM. A good example would be componentDidMount() – a lifecycle method that runs after the component is mounted and rendered to the DOM. It is great when you want to do an interval function or an asynchronous request. Example:
    componentDidMount() {
              fetch(url).then(res => {
            // Handle response in the way you want.
           // Most often with editing state values.
       })
    }

2. Updating, which involves methods for updating components in the DOM.
   The componentDidUpdate() render method is called right after the updating happens. This one is called always except for the initial render. That’s a good place to interact with a non-reactive environment. It’s a good idea to make http requests here. 

    You can call setState() in this method to enqueues changes to the component state. but it is very important to wrap that in some condition to avoid an infinite loop (doesn’t matter if state has the same values or not). If there is no condition, the process goes as follows:
    1. You call setState() in the componentDidUpdate() method.
    2. The component is updated.
    3. componentDidUpdate() is invoked.
    4. setState() is called again …

    componentDidUpdate(prevProps, prevState) {
    // Always compare props or state
    if (this.props.counter !== prevProps.counter) {
        this.postCounter(this.props.counter);
    }
    }
   
3. Unmounting, that is removing a component from the DOM.
   componentWillUnmount() is invoked just before the component is removed from the DOM. You should use that to remove event listeners, clear intervals and cancel requests. In other words: all the needed cleanup.
   componentWillUnmount() {
	        document.removeEventListener("click", this.someFunction);
    }

**React component lifecycle with hooks**
You can take advantage of the useEffect hook to achieve the same results as with the componentDidMount, componentDidUpdate and componentWillUnmount methods. useEffect accepts two parameters. The first one is a callback which runs after render, much like in componentDidMount. The second parameter is the effect dependency array. If you want to run it on mount and unmount only, pass an empty array [].

**Class components vs functional components**
As you can see, both class components and hooks have their pros and cons. Does it mean that the choice is mostly a matter of personal preference? For the most part, that’s the case. But there are some things worth noting:

- If you are more used to functional programming, you will definitely enjoy using hooks.
- Developers can use functional components without having to convert them into class components.
- Despite the fact that hooks are really popular nowadays, there is nothing wrong with using class components. Everything that you can do with hooks can also be done with class components.
- There are also other related topics worth exploring to make your choice even more informed, including network requests, choosing the only required method, child component issues and other React elements.
- Class components aren’t deprecated and are not going to be anytime soon so use them if that style suits you more.

[life cycle](https://tsh.io/blog/react-component-lifecycle-methods-vs-hooks/)