# 11-June-2022- 32th class reading notes:


## React Native

### Learn the Basics
React Native is like React, but it uses native components instead of web components as building blocks. So to understand the basic structure of a React Native app, you need to understand some of the basic React concepts, like JSX, components, state, and props. If you already know React, you still need to learn some React Native specific stuff, like the native components. This tutorial is aimed at all audiences, whether you have React experience or not.

First of all, we need to import React to be able to use JSX, which will then be transformed to the native components of each platform.
On line 2, we import the Text and View components from react-native

**Components**
So this code is defining HelloWorldApp, a new Component. When you're building a React Native app, you'll be making new components a lot. Anything you see on the screen is some sort of component.

**Props**
Most components can be customized when they are created, with different parameters. These creation parameters are called props.

**State**
Unlike props that are read-only and should not be modified, the state allows React components to change their output over time in response to user actions, network responses and anything else.

**What's the difference between state and props in React?**
In a React component, the props are the variables that we pass from a parent component to a child component. Similarly, the state are also variables, with the difference that they are not passed as parameters, but rather that the component initializes and manages them internally.

[react-itroduction](https://reactnative.dev/docs/tutorial)
[getting-starting](https://reactnative.dev/docs/getting-started)

### ExpoKit

    ExpoKit is an Objective-C and Java library that allows you to use the Expo platform and your existing Expo project as part of a larger standard native project -- one that you would normally create using Xcode, Android Studio, or react-native init.

**What is this for?**
If you created an Expo project and you want a way to add custom native modules, this guide will explain how to use ExpoKit for that purpose.
Normally, Expo apps are written in pure JS and never "drop down" to the native iOS or Android layer. This is core to the Expo philosophy and it's part of what makes Expo fast and powerful to use.
However, there are some cases where advanced developers need native capabilities outside of what Expo offers out-of-the-box. The most common situation is when a project requires a specific Native Module which is not supported by React Native Core or the Expo SDK.
In this case, Expo allows you to eject your pure-JS project from the Expo iOS/Android clients, providing you with native projects that can be opened and built with Xcode and Android Studio. Those projects will have dependencies on ExpoKit, so everything you already built will keep working as it did before.
We call this "ejecting" because you still depend on the Expo SDK, but your project no longer lives inside Expo Go. You control the native projects, including configuring and building them yourself.

### Should I eject to ExpoKit?

**You might want to eject if:**
    Your Expo project needs a native module that Expo doesn't currently support. We're always expanding the Expo SDK, so we hope this is never the case. But it happens, especially if your app has very specific and uncommon native demands.
**You should not eject if:**
- All you need is to distribute your app in the iTunes Store or Google Play. Expo can build binaries for you in that case. If you eject, we can't automatically build for you any more.
- You are uncomfortable writing native code. Ejected apps will require you to manage Xcode and Android Studio projects.
- You enjoy the painless React Native upgrades that come with Expo. After your app is ejected, breaking changes in React Native will affect your project differently, and you may need to figure them out for your particular situation.
- You require Expo's push notification services. After ejecting, since Expo no longer manages your push credentials, you'll need to manage your own push notification pipeline.
- You rely on asking for help in the Expo community. In your native Xcode and Android Studio projects, you may encounter questions which are no longer within the realm of Expo.

**Instructions**

1. Install Expo CLI
If you don't have it, run npm install -g expo-cli to get our command line library.
2. Make sure you have the necessary configuration options in app.json
3. Eject
4. Set up and Run your native project
5. Make native changes
6. Distribute your app

[expo](https://expo.dev/)
[expo.dev](https://snack.expo.dev/)













[Redux Thunk](https://youtu.be/9zySeP5vH9c)


[gh-pages](https://marah-jaradat.github.io/advanced-js-reading-notes/)

[My-repo](https://github.com/marah-jaradat/advanced-js-reading-notes/blob/gh-pages/31-day/31-readme.md)