# Introduction

This tutorial is my attempt at learning React. It will document the journey and have pointers to the resources used. The primary resource is a YouTube tutorial by _Programming with Mosh_. You can find it [here](https://www.youtube.com/watch?v=SqcY0GlETPk)

## Prerequisites

To learn REACT, you need a good understanding of the following web technologies:

- HTML
- CSS
- JavaScript
- TypeScript (essential but not a deal-breaker)

## What I need to Know

I don't know TypeScript. I would do well to know it. However, Mosh promised to introduce the learner to TS concepts, so that shouldn't be a point of worry.

# What is React?

React is a JS library for creating user interfaces. It was created at Facebook in 2011 and is currently the most popular JS library for front-end development.

It was created to simplify creating and manipulating DOM objects. It does this through a concept called Components. Instead of creating DOM elements and writing code to target them, in React, a higher-level concept called Components is used to abstract the DOM manipulation process. A developer works with Components, and React creates and handles the DOM manipulation automatically.

# Setting Up a Development Environment

To use React, you need to have `nodejs` installed. This tutorial requires you to have at least version 16 or higher. You can check the version by running `node -v` on the commandline.

# Creating A React App

There are two ways of creating a react app. You can use Create React App (CRA) which is the official tool provided by the React Team. Alternatively, you can use Vite - a tool which is popular for providing a simpler mechanism for creating a React App.

To create a React app using Vite, you can use
`npm create vite@latest`
`npm create vite@4.1.0`

The first one uses the latest version of Vite, and the second one uses a specific version of Vite.

This will create the app, and ask you for a project name. For instance, if the project name is _react-app_, afer set up, you will be instructed to take three steps:
`cd react-app` (move to the project directory)
`npm install` (install all the required packages)
`npm run dev` (start the development server)

Starting the develomept server will output something which looks as follows:
VITE v4.4.2 ready in 6944 ms
->Local: http://localhost:5137
->Network: use --host to expose
->press h to show help

When you open the URL provided on a web-browser, you will see the default page of your React App. Yay!!!

# React Folder Structure

A React App is composed of a files which are organized according to a unique file-structure. Understanding this structure is essential for mastering React.

_node_modules_ : This is where all the third-party libraries used by React are stored. You never have to touch this.

_public_ : This is where the public assets on the website e.g. images, videos, svg files, etc reside.

_src_ : This is the source code of the application.

_index.html_ : This file contains a div `<div id="root">` which is the root interface of the app. Below that, there is `<script src="/src/main.tsx>` which is the entry point to the application.

_package.json_ : This contains information about the project e.g. name, version, dependencies, etc

_tstconfig.json_ : This is a TypeScript configuration file. It tells the TS compiler how to convert the code to JS. For the most part, you never have to touch this file unless you're an advanced user.

_vite.config.ts_ : This is a configuration file for Vite. You may never have to touch this file.

# Creating A React Component

1. Add a new file in the src folder with a .tsx extension e.g. Message.tsx
2. Define a function in using PascalCasing as the name e.g. function Message(){}
3. Use JSX syntax to define a page element and a 'return' statement to return it
4. Export the component

Here is how the code inside the Message.tsx would be defined

```
function Message(){
    return <h1> Hello World <h1>
}

export default Message
```

# Adding A React Component to the App

To add a react component to the App, execute the following steps

1. Open the App.tsx document
2. Import the target Component
3. Add the Component inside the App() function
4. Export the App function

Here is how App.tsx would look if you add only the Message Component

import Message from "./Message"
function App(){
return <div>Message</div>
}

export default App

# Major Steps

Here are the major steps required to make a React Project:
