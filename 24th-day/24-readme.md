
# 16-May-2022- 23th class reading notes:

## Context API - Behaviors:

### **What is a Context?**

    Context API can solve many problems that modern applications face, related to state management, for example, props drilling. Many solutions can solve state management issues and props drilling, but they may increase your build size and compromise your app performance. Context API is a React built-in feature, so we don’t have to worry about performance overhead and library installing issues. 

    The props drilling problem occurs when you pass a prop somewhere down the tree. When a project grows, data passing through props becomes chaotic, making the code more vulnerable and complex. To tackle this problem, we use Context API. 

    Note: Many other state management libraries are also available, but we will see them in another blog.

**Here are a few benefits of Context API that give it an edge:**

1. The Context API helps share data between components which you can’t easily share with props, for example, complex data objects.  
2. React Context API provides a way to send data like userid, auth, and theme data through the component tree without sending any props manually at every level. 
3. We can also share specific states with multiple components instead through props manually. In some use cases, ideal for theming, localization, authentication etc.

**There are some other concepts we should understand before continuing.**

1. Provider 
    - The Provider component helps wrap the components which have access to our context.
    - The Provider component receives a prop called “value,”, which can be accessed from all the components wrapped inside the Provider. 
    - Value attribute gets default values for the Provider.
2. Consumer 
    - After wrapping all the components  that need access to context with the Provider component, you should tell which component is going to consume that data. 
    - The Consumer component allows a component to subscribe to context change. The consumer components allow to use data from the context. 
3. Dynamic Context 
    - The function which allows consumers to update the context in our case “setLoggedIn” function, is a context updater that will update our context according to the given value. 
  
### **USE CASES OF CONTEXT API (REAL WORLD APPLICATIONS OF CONTEXT API)**

**1: Authentication**
The most common use case of context API is we can authenticate the user and control the navigation according to the auth response, as we did in this blog. 

**2: Theming** 
We can customize the theme of our app on a specific page. Let’s assume we have to design an app that should have a dark and light mode. We want to change the theme of the app according to the user need to use theming objects, e.g., mode, color and in context state. These all-context states can be used in any view or page where we want to change the theme.

**3: Responsiveness** 
If we are designing an app that is super responsive on every device, mobile, tab, and large screens, then we will detect the device screen size and orientation, save the screen state in the context object. When the device screen context is available to all components, we can adjust them according to the screen state. 
 
### **CONTEXT API VS USECONTEXT** 

**Context API** 
The Context API is the React feature used for solving props drilling problems. We have already discussed props drilling in the above section. In Context API, we give data access to a component tree at the start to end level instead of using props. 

**useContext** 
The useContext is the React hook, used in context API to consume the context state or object. There are two options for getting the context object. We can get the context object from Context Consumer or useContext Hook. UseContext Hook is an exquisite, more excellent way to get the context object with less code. 

### **ADVANTAGES AND DISADVANTAGES OF CONTEXT API**

**Advantages** 
- React built-in feature 
- Easy to implement 
- No overhead or performance compromise 
- Props drilling problem solution 
  
**Disadvantage** 
- Not a suitable option for large projects. 
- Automatically re-renders components when the context state changes 

[react-context-more-links](https://github.com/diegohaz/awesome-react-context)

[gh-pages](https://marah-jaradat.github.io/advanced-js-reading-notes/)

[My-repo](https://github.com/marah-jaradat/advanced-js-reading-notes/blob/main/24th-day/24-readme.md)

