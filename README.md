# React Tutorial

All tutorials are from the Complete React Tutorial on the Net Ninja YouTube channel, [link is here](https://www.youtube.com/playlist?list=PL4cUxeGkcC9gZD-Tvwfod2gaISzfRiP9d).

## Table of Contents  
- [React Tutorial](#react-tutorial)
  - [Table of Contents](#table-of-contents)
  - [1. Creating a React App](#1-creating-a-react-app)
    - [1.1. Steps for creating a React App:](#11-steps-for-creating-a-react-app)
    - [1.2. What does the starter React Project contain?](#12-what-does-the-starter-react-project-contain)
    - [1.3. What can we remove from the starter React App?](#13-what-can-we-remove-from-the-starter-react-app)
  - [2. React Dev Tools](#2-react-dev-tools)
  - [3. JSX](#3-jsx)
    - [3.1. What is JSX?](#31-what-is-jsx)
    - [3.2. How to use JSX?](#32-how-to-use-jsx)
      - [3.2.1. JS expressions in JSX](#321-js-expressions-in-jsx)
      - [3.2.2. JS expressions in HTML attributes](#322-js-expressions-in-html-attributes)
      - [3.2.3. JS functions and objects](#323-js-functions-and-objects)
  - [4. Components](#4-components)
    - [4.1. What are Components?](#41-what-are-components)
    - [4.2. How to create Function Components](#42-how-to-create-function-components)
    - [4.3. How to create Class Components](#43-how-to-create-class-components)
    - [4.4. Function Components vs. Class Components](#44-function-components-vs-class-components)
    - [4.5. Tutorial](#45-tutorial)
      - [4.5.1 Multiple Components](#451-multiple-components)
      - [4.5.2. Adding Styles](#452-adding-styles)
  - [5. Props](#5-props)
    - [5.1. What are Props?](#51-what-are-props)
    - [5.2. How to use Props](#52-how-to-use-props)
    - [5.3. Default Props](#53-default-props)
    - [5.4. Tutorial](#54-tutorial)
      - [5.4.1. Props \& Reusable Components](#541-props--reusable-components)
      - [5.4.2. Reusing Components with different Props](#542-reusing-components-with-different-props)
      - [5.4.3. Functions as Props](#543-functions-as-props)
  - [6. State](#6-state)
    - [6.1. What is State?](#61-what-is-state)
    - [6.2. How to use State in Function Components](#62-how-to-use-state-in-function-components)
    - [6.3. Tutorial](#63-tutorial)
  - [7. Event Handling](#7-event-handling)
    - [7.1. What is Event Handling?](#71-what-is-event-handling)
    - [7.2. How to Handle Events in ReactJS](#72-how-to-handle-events-in-reactjs)
    - [7.3. Passing Arguments to Event Handlers](#73-passing-arguments-to-event-handlers)
    - [7.4. Tutorial](#74-tutorial)
  - [8. Hooks](#8-hooks)
    - [8.1. What are Hooks in ReactJS?](#81-what-are-hooks-in-reactjs)
    - [8.2. Why do we use Hooks?](#82-why-do-we-use-hooks)
    - [8.3. Hook Rules](#83-hook-rules)
    - [8.4. useState Hook](#84-usestate-hook)
    - [8.5. useEffect Hook](#85-useeffect-hook)
    - [8.6. Custom Hooks](#86-custom-hooks)
    - [8.7. Tutorial](#87-tutorial)
      - [8.7.1. Outputting Lists](#871-outputting-lists)
      - [8.7.2. Using JSON Server](#872-using-json-server)
      - [8.7.3. Fetching Data in useEffect](#873-fetching-data-in-useeffect)
      - [8.7.4. JSX Conditionals](#874-jsx-conditionals)
      - [8.7.5. Conditional Loading Message](#875-conditional-loading-message)
      - [8.7.6. Handling Fetch Errors](#876-handling-fetch-errors)
      - [8.7.7. Making a Custom Hook](#877-making-a-custom-hook)
      - [8.7.8. useEffect Cleanup](#878-useeffect-cleanup)
      - [8.7.9. Re-using a Custom Hook](#879-re-using-a-custom-hook)
  - [9. Lifecycle Methods](#9-lifecycle-methods)
    - [9.1. Mounting Phase](#91-mounting-phase)
    - [9.2. Updating Phase](#92-updating-phase)
    - [9.3. Unmounting Phase](#93-unmounting-phase)
    - [9.4. Tutorial](#94-tutorial)
  - [10. React Router](#10-react-router)
    - [10.1. Tutorial](#101-tutorial)
      - [10.1.1. The React Router](#1011-the-react-router)
      - [10.1.2. Route Parameters](#1012-route-parameters)
  - [11. Web Forms](#11-web-forms)
    - [11.1. Tutorial](#111-tutorial)
      - [11.1.1. Controlled Inputs](#1111-controlled-inputs)
      - [11.1.2. Submit Events](#1112-submit-events)
      - [11.1.3. Sending POST Requests](#1113-sending-post-requests)
      - [11.1.4. Programmatic Redirects](#1114-programmatic-redirects)
      - [11.1.5. Deleting Blogs](#1115-deleting-blogs)
      - [11.1.6. 404 Pages](#1116-404-pages)
  - [12. Server-side Rendering](#12-server-side-rendering)
  - [13. Testing](#13-testing)

## 1. Creating a React App

### <ins>1.1. Steps for creating a React App:</ins>
1. Need node installed. Check version with `node -v`. If no version, install using brew with `brew install node`.
2. Run command `npx create-react-app app-name` in terminal to bootstrap a starter react project called 'app-name' in current directory.
3. Change directory to the newly created react project and run command `code .` to open current directory (starter react project) in VSCode.
4. To run react app in dev mode run the command `npm start` and the application will run locally at at localhost:3000.

### <ins>1.2. What does the starter React Project contain?</ins>
There are a series of folders and files within the starter react project.

![React App Folder Structure](/images/react-app-folder-structure.png)
![React App Files](/images/react-app-files.png)

node_modules:

- The node_modules folder contains all of the project dependencies, including the react library. Any packages or libraries installed in the future will always be stored in this location.
- If you were to delete this folder, the react app would not run. This is because all of the project dependencies are no longer present.
- You may notice that sometimes when you download a React project from GitHub... the node_modules folder is not present. This is because the node_modules folder is added to .gitignore as it is very large in file size (due to all the dependencies and libraries it contains). As a result, it is not included in many GitHub react projects to save time in downloading/uploading projects.
- If the folder is missing from a React App, in the project root directory run `npm install`. This command looks at the package.json file which declares all of the project dependencies, and it re-installs them back into a node_modules folder!

public:

- The public folder contains all of the files that are public to the browser.
- The index.html file within the public folder is the entry-point of the react app in the browser. 
- All react code is injected into this 1 html file which is served to the browser. The exact location of this injection is in the div element with id="root".

src:

- The src folder contains 99% of the code you will write in react.
- App.js is a react component which contains some JSX elements, and in the future will hold other child components that you develop. 
- There are also other CSS and JS files within this folder.
- The index.js file is what kick starts the application. It is responsible for taking all of the JSX and React components created and injected into App.js return() method, and mounts them to the DOM via the id="root" div element in the index.html file (public folder).

.gitignore:

- This file is used for version control with git and contains the files and folders you want to be ignored when committing changes to the project and pushing these changes to the remote git repository.

package.json:

- This file contains all of the dependencies, scripts, and other configurations of the application/project.

package-lock.json:

- This file is essentially used to lock dependencies to a specific version number. This file is automatically generated (or re-generated) when there is a change in either the node_modules tree or package.json file.

README.md:

- This file is used for documentation of the project.

### <ins>1.3. What can we remove from the starter React App?</ins>
The starter react project comes with some default files that render the starter page but these can be removed, to help cleanup the project for the development of our own app.

<ins>Files to delete</ins>

src:
- App.test.js
- setupTests.js
- logo.svg
- reportWebVitals.js
- index.css OR App.css (depends on project size and purpose)

public:
- All files except index.html

<ins>Code to remove/edit</ins>

src: 
- logo.svg import in App.js 
- reportWebVitals.js import and corresponding code in index.js
- index.css import in index.js (OR App.css import in App.js)
- clear the code inside of div in App.js (lines 6 to 19)
- convert App() function to arrow function in App.js
- keep index.css file (OR App.css) but clear the code.

public: 
- remove links to deleted files in index.html (line 5, 12 & 17) 
- remove comments in index.html
- change Title to something related to your project

<ins>Useful Links:</ins>
<br/>
Link to: [How to create a React App & File Cleanup](https://www.youtube.com/watch?v=PAqbIbdvTuU)
<br/>
Link to: [Full React Tutorial #2 - Creating a React Application](https://www.youtube.com/watch?v=kVeOpcw4GWY&list=PL4cUxeGkcC9gZD-Tvwfod2gaISzfRiP9d&index=2)

## 2. React Dev Tools
React Dev Tools is an extension used in Chrome which adds more features to our Chrome Dev Tools. It allows you to inspect a React tree, including the component hierarchy, props, state, and more. All you have to do to use it, is open the Chrome Dev Tools menu and switch to either the 'Components' or 'Profiler' tab.

Link to: [Full React Tutorial #9 - Intro to React Dev Tools](https://www.youtube.com/watch?v=rb1GWqCJid4&list=PL4cUxeGkcC9gZD-Tvwfod2gaISzfRiP9d&index=9)

## 3. JSX

### 3.1. What is JSX?

JSX (JavaScript XML) is a syntax extension for JavaScript that allows you to mix HTML-like syntax with JavaScript logic within your JavaScript code. This makes it easier to create and manipulate complex user interfaces in ReactJS. It is not a separate language, but rather a syntax that is transformed into regular JavaScript at compile-time.

### 3.2. How to use JSX?

#### 3.2.1. JS expressions in JSX
To use JSX in your ReactJS code, you simply write HTML-like syntax within your JavaScript code, using curly braces to embed JavaScript expressions. For example:

```js
// App.js
import React from 'react';

function App() {
  const name = 'John';
  const age = 25;

  return (
    <div>
      <h1>Hello, {name}!</h1>
      <p>You are {age} years old.</p>
    </div>
  );
}

export default App;
```

In this example, we're using JSX to render a simple greeting to the user. We're using curly braces to embed JavaScript expressions within the HTML-like syntax. The expressions are evaluated at runtime and their values are rendered to the screen.

#### 3.2.2. JS expressions in HTML attributes
JSX also allows you to use JavaScript expressions within HTML attributes. For example:

```js
// App.js
import React from 'react';

function App() {
  const url = 'https://www.google.com';

  return (
    <div>
      <a href={url}>Go to Google</a>
    </div>
  );
}

export default App;
```

In this example, we're using JSX to create a link to Google. We're using curly braces to embed the value of the url variable within the href attribute of the anchor tag.

#### 3.2.3. JS functions and objects
JSX also supports the use of JavaScript functions and objects. For example:

```js
// App.js
import React from 'react';

function App() {
  const person = {
    name: 'John',
    age: 25
  };

  function formatName(person) {
    return `${person.name} (${person.age} years old)`;
  }

  return (
    <div>
      <h1>Hello, {formatName(person)}!</h1>
    </div>
  );
}

export default App;
```

NOTE: Inside functions, regular JavaScript code is valid as long as it is preceding the return() method, where JSX is written. Of course here, any JavaScript expression you want to embed within the return() method must be wrapped in curly braces { }.
<br/>
<!-- NOTE: JSX cannot interpret booleans and objects within the curly braces where we embed JavaScript expressions { }. -->

In this example, we're using a JavaScript object and function to format the name and age of a person. We're using JSX to render the formatted name to the screen.

That's a basic introduction to JSX in ReactJS. JSX makes it easier to create and manipulate complex user interfaces in ReactJS by allowing you to mix HTML-like syntax with JavaScript logic.

## 4. Components

### 4.1. What are Components?
Components are the building blocks of ReactJS applications. They are reusable pieces of code that encapsulate the behavior and appearance of a section of a UI. Components contain their own template and logic for that piece of content. Using the component as a factory, an infinite number of component instances can be created.

![React Components](/images/react-components.png)

In ReactJS there are two types of components, function components and class components. Function components are simpler and easier to use. Whereas class components are very cumbersome to use and are not used as much in modern React apps, despite being able to provide more advanced customization. 

### 4.2. How to create Function Components
To create a function component, you simply define a JavaScript function that returns JSX code. For example:

```js
// Greeting.js
import React from 'react';

function Greeting(props) {
  return <h1>Hello, {props.name}!</h1>;
}

export default Greeting;
```

In this example, we're creating a simple function component called Greeting. The component accepts a single prop called name, and uses it to render a greeting to the user.

To use this component in another part of your code, you simply import it and use it like any other HTML tag. For example:

```js
// App.js
import React from 'react';
import Greeting from './Greeting';

function App() {
  return (
    <div>
      <Greeting name="John" />
    </div>
  );
}

export default App;
```

In this example, we're using the Greeting component to render a greeting to the user. We're passing a prop called name with the value "John" to the component.

### 4.3. How to create Class Components
To create a class component, you define a class that extends the React.Component class. You must also define a render() method that returns JSX code. For example:

```js
// Greeting.js
import React from 'react';

class Greeting extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}!</h1>;
  }
}

export default Greeting;
```

In this example, we're creating the same Greeting component as before, but as a class component. The render() method returns the JSX code that we want to render to the screen.

To use this component in another part of your code, you use it like any other HTML tag. For example:

```js
// App.js
import React from 'react';
import Greeting from './Greeting';

function App() {
  return (
    <div>
      <Greeting name="John" />
    </div>
  );
}

export default App;
```

In this example, we're using the Greeting component to render a greeting to the user. We're passing a prop called name with the value "John" to the component.

That's a basic introduction to Components in ReactJS. Components are the building blocks of ReactJS applications, and allow you to encapsulate the behavior and appearance of a part of a user interface in a reusable and modular way.

### 4.4. Function Components vs. Class Components

Before Hooks (pre React 16.8) function components were basically just a render method. That meant if you wanted to use state, refs, or logic at lifecycle events like mount, unmount, or update you would need to use the class syntax.

Functional components with hooks are shorter than the equivalent class syntax. Everything else being equal, it’s very advantageous to have fewer lines of code. This makes things much more legible and maintainable.

Functional components are also much easier to understand for people with basic knowledge of JavaScript. Earlier versions of React required frequent use of “bind” which is confusing for many. Class components rely on the “this” keyword which is also an added difficulty. Functional components can typically avoid using "this", or "bind"/"call"/"apply".

Furthermore, it’s interesting to see the hooks that React developers favoured as the main hooks. For class components, an equivalent to these are the lifecycle methods which have remained stable for most of React’s history. The hooks that come out of the box with React encourage developers into using React in a slightly different way. useEffect for instance essentially replaces componentDidMount, componentDidUpdate and componentDidUnmount. Another example is useReducer, which can dispense the user from setting up redux in your React application.

<ins>Summary:

Function components are becoming increasingly popular over class components in ReactJS for several reasons:

1. Simplicity: Function components are simpler than class components. They are shorter, easier to read and write, and require less boilerplate code.
2. Performance: Function components are generally faster than class components because they don't need to create a new instance of a component and don't have the overhead of managing state and lifecycle methods.
3. Hooks: React Hooks were introduced in React 16.8 and are only available for function components. Hooks provide a way to use state and other React features within a function component, making them even more powerful and flexible.
4. Functional programming: Function components are more aligned with functional programming principles. They are pure functions that take input and return output without modifying external state. This makes them easier to reason about and test.

Overall, function components offer a simpler and more performant way to create React applications. While class components are still used in many legacy applications and have their place, function components are becoming the standard in modern React development.

### 4.5. Tutorial

A NavBar component will contain a template which makes up the HTML and also any JS logic. For example, a JS function that runs if a logout HTML button is clicked! React components allows us to implement these features very easily.

React requires that the first letter of components be capitalized. For example, App.js contains the function App(). JSX will use this capitalization to tell the difference between an HTML tag and a component instance. If the first letter of a name is capitalized, then JSX knows it’s a component instance; if not, then it’s an HTML element. In the background, a transpiler called babel converts all of the JSX template to HTML, and it renders it to the DOM. A class component’s return() method must return JSX, including a mix of HTML elements and custom React components.

in JSX, we use className instead of class (like in HTML) because class is a reserved keyword in JS! Babel converts this into class when the code is transpiled from JSX to HTML in the DOM.

In React versions less than 17, you need to import React at the top of the component file. In React v17 and above, you do not need it.

At the end, we always export our function component, this is so we can import and use them in other files. For example, the App function component in App.js is exported, and in index.js it is imported and used. For example:

App.js:
```js
import './App.css';

const App = () => {

  const sayHello = () => {
    alert('Hello!');
  }

  return (
    <div className="App">
      <h1>Hello</h1>
      <button onClick={sayHello}>Click me</button>
    </div>
  );
}

export default App;
```

index.js:
```js
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```

Browser View:

![Section 2 Browser View Before](/images/section-2-browser-view-before.png)
![Section 2 Browser View After](/images/section-2-browser-view-after.png)

#### 4.5.1 Multiple Components

App.js is known as the root component of the application. This means it is the first component that gets rendered to the DOM and it sits at the very top of our app. It is the component that the index.js file renders.

In React, our components are structured in a manner that makes up a tree. The root component sits at the top of the tree. Any other component is nested inside of this component. If further components are made, these can be nested in those already nested components, and so on.

![React Component Tree](/images/react-component-tree.png)

In this tutorial we will create the Navbar.js and Home.js component. A component is simply a function that returns a JSX template, and this function is exported at the bottom of the code. It is common to keep each React component in its own file, export it, and import it wherever else it is needed. This file organization helps make components reusable. You don’t need to do this, but it’s a useful convention.

Use `rafce->` if ES7+ React Snippets extension is enabled. This will generate boilerplate code for a react arrow function component that is exported. Arrow functions are the preferred approach for declaring components by many modern React developers.

Navbar.js:
```js
import React from 'react'

const Navbar = () => {
  return (
    <nav className='navbar'>
        <h1>The Arsalaan Blog</h1>
        <div className="links">
            <a href="/">Home</a>
            <a href="/create">New Blog</a>
        </div>
    </nav>
  )
}

export default Navbar
```

Home.js:
```js
import React from 'react'

const Home = () => {
  return (
    <div className="home">
        <h2>Homepage</h2>
    </div>
  )
}

export default Home
```

App.js:
```js
import './App.css';
import Navbar from './Navbar';
import Home from './Home';

const App = () => {
  return (
    <div className="App">
      <Navbar />
      <div className="content">
        <Home />
      </div>
    </div>
  );
}

export default App;
```

Browser View:

![Section 4 Browser View](/images/section-4-browser-view.png)

NOTE: index.js and index.html remain the same

index.js:
```js
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";

const root = ReactDOM.createRoot(document.getElementById("root"));
root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);

```

index.html:
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <meta name="theme-color" content="#000000" />
    <meta
      name="description"
      content="Web site created using create-react-app"
    />
    <title>React Tutorial</title>
  </head>
  <body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
  </body>
</html>
```

#### 4.5.2. Adding Styles

Now that we have our 3 components: the root component (App.js), the Navbar and Home. It is now time to add some CSS styling! App.js imports App.css by default. All styles declared here will not only apply to the App.js component, but also to any component that is in the browser at that time. This is because CSS takes the stylesheet, and applies it to the head of the index.html file.

Having separate CSS files for separate components is done mainly for organisation purposes when workng on large projects. For smaller projects, a single CSS file that contains all the styling is sufficient. Consider it as a 'global' stylesheet that applies to all components! The index.css file is then imported into the index.js file, which takes all of those styles and adds them to the head of the webpage.

index.css:
```css
/* Google Font */
@import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600;700&display=swap');

/* base styles */
* {
  margin: 0;
  font-family: "Quicksand";
  color: #333;
}
.navbar {
  padding: 20px;
  display: flex;
  align-items: center;
  max-width: 600px;
  margin: 0 auto;
  border-bottom: 1px solid #f2f2f2;
}
.navbar h1 {
  color: #f1356d;
}
.navbar .links {
  margin-left: auto;
}
.navbar a {
  margin-left: 16px;
  text-decoration: none;
  padding: 6px;
}
.navbar a:hover {
  color: #f1356d;
}
.content {
  max-width: 600px;
  margin: 40px auto;
  padding: 20px;
}
```

Browser View:

![Section 5 Browser View](/images/section-5-browser-view.png)

You can also add inline styling, like in HTML. In JSX, the value of style can be a dynamic value of type object. But, unlike CSS where hyphens separate words, in JSX we use camel case. This is because what is being written inside the curly braces { } is interpreted as JS, and a hyphen would be interpreted as a minus symbol. For example:

Navbar.js:
```js
import React from 'react'

const Navbar = () => {
  return (
    <nav className='navbar'>
        <h1>The Arsalaan Blog</h1>
        <div className="links">
            <a href="/">Home</a>
            <a href="/create" style={{
                color: "white",
                backgroundColor: '#f1356d',
                borderRadius: '8px'
            }} >New Blog</a>
        </div>
    </nav>
  )
}

export default Navbar
```

NOTE: style attribute is not included in actual file, only shown for demonstration purposes here.

## 5. Props

### 5.1. What are Props?
Props (short for "properties") are a way to pass data from a parent component to a child component in ReactJS. They are similar to HTML attributes or function arguments. In ReactJS, props are read-only, meaning that a child component cannot modify the props that it receives from its parent.

### 5.2. How to use Props
To pass props to a child component, you simply add them as attributes when you render the child component. For example, let's say we have a parent component called App and a child component called Child:

```js
// App.js

import React from 'react';
import Child from './Child';

function App() {
  return (
    <div>
      <Child name="John" age={25} />
    </div>
  );
}

export default App;

// Child.js

import React from 'react';

function Child(props) {
  return (
    <div>
      <p>Name: {props.name}</p>
      <p>Age: {props.age}</p>
    </div>
  );
}

export default Child;
```

In this example, we're passing two props to the Child component: name and age. The values for these props are hardcoded in the App component, but they could also be dynamically generated based on some other data or logic.

In the Child component, we're using the props object to access the values of the name and age props. We're using curly braces to embed the values within the JSX code.

### 5.3. Default Props
You can also set default values for props in case they are not passed from the parent component. To set default props, you can use the defaultProps property on the child component. For example:

```js
// Child.js

import React from 'react';

function Child(props) {
  return (
    <div>
      <p>Name: {props.name}</p>
      <p>Age: {props.age}</p>
    </div>
  );
}

Child.defaultProps = {
  name: 'Unknown',
  age: 0
}

export default Child;
```

In this example, we're setting default values for the name and age props to "Unknown" and 0, respectively. If these props are not passed from the parent component, these default values will be used instead.

That's a basic introduction to Props in ReactJS. Props are a powerful way to pass data between components and create more dynamic and reusable code.

### 5.4. Tutorial
#### 5.4.1. Props & Reusable Components
In our project, if we are building a blog website, we may have the list of blogs in various locations of the website. There is going to be different places in the code that will be using the same logic of cycling through the blogs list and outputting a blog preview for each one.

If we do this, we would be repeating the code in Home.js multiple times in different components for different pages. Instead, we can make this template its own reusable component! We can cut the logic and paste it into a BlogList component. Aside from being reusable, we will see how we can pass in different data into the reusable component each time we use it. This is done in the form of props. For example, we may show all blogs in the homepage, but on a search page, we might only show the blogs that match a 'search term'. The structure will be the same but the data input will be different.

Firstly we are creating a new component to store the reusable template. We use props to pass the data into the BlogList component. Props are a way of passing through data from a parent component to a child component. Components can pass information to other components. When one component passes information to another, it is passed as props through one or more attributes.

Home.js:
```js
import React from 'react'
import { useState } from 'react';
import BlogList from './BlogList';

const Home = () => {

   const [blogs, setBlogs] = useState([
    { title: 'My new website', body: 'lorem ipsum...', author: 'mario', id: 1},
    { title: 'Welcome party!', body: 'lorem ipsum...', author: 'yoshi', id: 2},
    { title: 'Web dev top tips', body: 'lorem ipsum...', author: 'mario', id: 3}
   ]);
    
  return (
    <div className="home">
        <BlogList blogs={blogs} title="All Blogs!" />
    </div>
  )
}

export default Home
```

BlogList.js:
```js
import React from 'react'

const BlogList = (props) => {

    const blogs = props.blogs;
    const title = props.title;

  return (
    <div className="blog-list">
        <h2>{ title }</h2>
        {blogs.map((blog) => (
            <div className="blog-preview" key={blog.id}>
                <h2>{ blog.title }</h2>
                <p>Written by {blog.author}</p>
            </div>
        ))}
    </div>
  )
}

export default BlogList
```

`blogs={blogs}` is a prop. Any props passed as arguments are automatically attached to the props object, which we can access.

So, this is how we get a component to take in props (data), and then use that data inside that component. This makes that component more reusable!

NOTE: Instead of capturing the props individually as 

`const blogs = props.blogs;`
`const title = props.title;`

We can destructure the props directly in the function arguments.
So instead we get

BlogList.js:
```js
import React from 'react'

const BlogList = ({ blogs, title }) => {
  return (
    <div className="blog-list">
        <h2>{ title }</h2>
        {blogs.map((blog) => (
            <div className="blog-preview" key={blog.id}>
                <h2>{ blog.title }</h2>
                <p>Written by {blog.author}</p>
            </div>
        ))}
    </div>
  )
}

export default BlogList
```

Browser View:
![Section 10 props](/images/section-10-props.png)

#### 5.4.2. Reusing Components with different Props
We can reuse components multiple times in ur applications, each time with different props (data). Here we will have 2 components of BlogList. One with all blogs and another with just mario's blogs. Here we need to add some JS logic to filter only the blogs who have an author of mario (also can be described as filtering out the blogs that do NOT have an author of mario).

The .filter() method will execute a callback function. If the condition for the current is true, it keeps it in the array. If we return false, it filters it out of the array. The function then returns a new array with only the items that did not get filtered out, and this array itself is returns as a prop.

These reusable components that take in props (paired with .filter() method) are very useful and can be used for something like a search page, whereby the title matches the search term for example.

Home.js:
```js
import React from 'react'
import { useState } from 'react';
import BlogList from './BlogList';

const Home = () => {

   const [blogs, setBlogs] = useState([
    { title: 'My new website', body: 'lorem ipsum...', author: 'mario', id: 1},
    { title: 'Welcome party!', body: 'lorem ipsum...', author: 'yoshi', id: 2},
    { title: 'Web dev top tips', body: 'lorem ipsum...', author: 'mario', id: 3}
   ]);
    
  return (
    <div className="home">
        <BlogList blogs={blogs} title="All Blogs!" />
        <BlogList blogs={blogs.filter((blog) => blog.author === 'mario' )} title="Mario's blogs" />
    </div>
  )
}

export default Home
```

BlogList.js:
```js
import React from 'react'

const BlogList = ({ blogs, title }) => {
  return (
    <div className="blog-list">
        <h2>{ title }</h2>
        {blogs.map((blog) => (
            <div className="blog-preview" key={blog.id}>
                <h2>{ blog.title }</h2>
                <p>Written by {blog.author}</p>
            </div>
        ))}
    </div>
  )
}

export default BlogList
```

Browser View:
![Section 11 reusing](/images/section-11-reusing.png)

#### 5.4.3. Functions as Props
We now want to be able to delete these blogs by clicking on a button.
First we need to add a button to each blog list item. Also, we need to give it a click event handler.

We need to create a handleDelete function that takes the blog id as an argument. We do not want to directly edit the blogs prop in the child component. Instead we use the 'setBlogs' method inside the parent component to update the state! So, we put our handleDelete logic inside of the setBlogs function, where both are within the parent component. Then we pass the handleDelete function through as a prop itself.

So, we add the handleDelete as a prop in the button, and remember to add this prop to the blogs and title already declared in the BlogList component. We use setBlogs to update the blogs and remove the blog with id.

Summary:
- when the "delete blog" button is clicked, the handleDelete function is invoked; 
- then inside the handleDelete function, the setBlogs function is invoked, thus changing the value of blogs; 
- because blogs as a state variable has changed, React re-renders the Home component; 
- When React re-renders the Home component, it also re-renders the BlogList component. 

Home.js:
```js
import React from 'react'
import { useState } from 'react';
import BlogList from './BlogList';

const Home = () => {

   const [blogs, setBlogs] = useState([
    { title: 'My new website', body: 'lorem ipsum...', author: 'mario', id: 1},
    { title: 'Welcome party!', body: 'lorem ipsum...', author: 'yoshi', id: 2},
    { title: 'Web dev top tips', body: 'lorem ipsum...', author: 'mario', id: 3}
   ]);

   const handleDelete = (id) => {
      const newBlogs = blogs.filter((blog) => blog.id !== id);
      setBlogs(newBlogs);
   }
    
  return (
    <div className="home">
        <BlogList blogs={blogs} title="All Blogs!" handleDelete={handleDelete}/>
    </div>
  )
}

export default Home
```

BlogList.js:
```js
import React from 'react'

const BlogList = ({ blogs, title, handleDelete }) => {
  return (
    <div className="blog-list">
        <h2>{ title }</h2>
        {blogs.map((blog) => (
            <div className="blog-preview" key={blog.id}>
                <h2>{ blog.title }</h2>
                <p>Written by {blog.author}</p>
                <button onClick={() => handleDelete(blog.id)}>delete blog</button>
            </div>
        ))}
    </div>
  )
}

export default BlogList
```

Browser View:
![Section 12 before](/images/section-12-before.png)
![Section 12 after](/images/section-12-after.png)

If we refresh the page, the blogs return. This is because we are re-running the code and it resets the state back to its initial value.

## 6. State
### 6.1. What is State?
State is a way to store and manage data in ReactJS components. It represents the internal state of a component and can be changed over time, usually as a result of user interactions or data changes.

State is one of the most important concepts in ReactJS, and is used to create dynamic and interactive user interfaces.

### 6.2. How to use State in Function Components
To use state in a function component, you need to use the useState hook provided by React. The useState hook is a function that returns an array with two elements: the current state value, and a function to update the state value.

Here's an example of how to use the useState hook in a function component:

```js
// Counter.js

import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  function handleClick() {
    setCount(count + 1);
  }

  return (
    <div>
      <h1>{count}</h1>
      <button onClick={handleClick}>Click me!</button>
    </div>
  );
}

export default Counter;
```

In this example, we're creating a simple function component called Counter. The component uses the useState hook to define a state variable called count, which is initially set to 0.

The component also defines a function called handleClick, which is called when the user clicks on the button. The handleClick function updates the count state by calling the setCount function with the new count value.

To use this component in another part of your code, you simply import it and use it like any other HTML tag. For example:

```js
// App.js

import React from 'react';
import Counter from './Counter';

function App() {
  return (
    <div>
      <Counter />
    </div>
  );
}

export default App;
```

In this example, we're using the Counter component to render a simple counter to the user.

NOTE: We will not be covering how to use State in Class Components.

That's a basic introduction to State in ReactJS. State allows you to create dynamic and interactive user interfaces by storing and managing data within ReactJS components.

Link to: [Full React Tutorial #8 - Using State (useState hook)](https://www.youtube.com/watch?v=4pO-HcG2igk&list=PL4cUxeGkcC9gZD-Tvwfod2gaISzfRiP9d&index=8)

### 6.3. Tutorial

When we talk about the 'state of a component' we are simply referring to the data being used by a component at that point in time. The data can be an array of values, booleans, string, objects, etc. 

What if we had variables or data that we wanted to change over time in reaction to some event (like a user clicking a button). In this project we will demonstrate how we can change the name shown in the browser by clicking a button by using the useState hook.

A hook in React is a special type of function that does a certain job. All hooks in React start with the term 'use'. The useState hook gives us a way to make a Reactive value, and also provides us with a way to change that value whenever we want.

useState() Hook Template:
```js
const [currentState, stateSetter] = useState(initialState);
```

The useState() Hook lets you add React state to function components. It should be called at the top level of a React function definition to manage its state. initialState is an optional value that can be used to set the value of currentState for the first render. The stateSetter function is used to update the value of currentState and rerender our component with the next state value.

NOTE: Must import useState function from react library.

Home.js:
```js
import React from 'react'
import { useState } from 'react';

const Home = () => {

    const [name, setName] = useState('mario');

    const handleClick = () => {
        setName('luigi')
    }

    
  return (
    <div className="home">
        <h2>Homepage</h2>
        <p>{ name }</p>
        <button onClick={handleClick}>Click me</button>
    </div>
  )
}

export default Home
```

Browser View (before and after clicking button):

![Section 7 useState before 1](/images/section-7-useState-before-1.png)
![Section 7 useState after 1](/images/section-7-useState-after-1.png)

NOTE: In React, many developers use a function as a component instead of a class. Function components receive props as a parameter.

In the example code, we show two equivalent components: one as a class and one as a function.

Example:
```js
// The two components below are equivalent.
class GreeterAsClass extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}!</h1>;
  }
}

function GreeterAsFunction(props) {
  return <h1>Hello, {props.name}!</h1>;
}
```

Another example:
Home.js:
```js
import React from 'react'
import { useState } from 'react';

const Home = () => {

    const [name, setName] = useState('mario');
    const [age, setAge] = useState(25);

    const handleClick = () => {
        setName('luigi')
        setAge(30);
    }

    
  return (
    <div className="home">
        <h2>Homepage</h2>
        <p>{ name } is {age} years old!</p>
        <button onClick={handleClick}>Click me</button>
    </div>
  )
}

export default Home
```

useState() may be called more than once in a component. This gives us the freedom to separate concerns, simplify our state setter logic, and organize our code in whatever way makes the most sense to us!

Browser View (before and after clicking button):

![Section 7 useState before 2](/images/section-7-useState-before-2.png)
![Section 7 useState after 2](/images/section-7-useState-after-2.png)

## 7. Event Handling

### 7.1. What is Event Handling?
Event handling is the process of capturing and responding to user actions, such as clicking a button, typing in a text field, or scrolling the page. In ReactJS, event handling is a core feature that allows you to create dynamic and interactive user interfaces.

### 7.2. How to Handle Events in ReactJS
In ReactJS, you can handle events by attaching event listeners to HTML elements, just like you would in plain JavaScript. However, there are a few differences in how event handling works in ReactJS.

Here's an example of how to handle events in ReactJS:

```js
// Button.js

import React from 'react';

function Button(props) {
  function handleClick(event) {
    console.log('Button clicked');
    console.log('Event:', event);
  }

  return (
    <button onClick={handleClick}>{props.text}</button>
  );
}

export default Button;
```
In this example, we're creating a simple function component called Button. The component takes a props object as an argument, which contains a text property that specifies the text to display on the button.

The component also defines a function called handleClick, which is called when the user clicks on the button. The handleClick function logs a message to the console, and also logs the event object that was generated by the click.

To use this component in another part of your code, you simply import it and use it like any other HTML tag. For example:

```js
// App.js

import React from 'react';
import Button from './Button';

function App() {
  return (
    <div>
      <Button text="Click me!" />
    </div>
  );
}

export default App;
```

In this example, we're using the Button component to render a simple button to the user.

### 7.3. Passing Arguments to Event Handlers
In some cases, you may want to pass additional arguments to an event handler function. To do this, you can define a separate function that returns the event handler function with the additional arguments.

Here's an example of how to pass arguments to an event handler function:
```js
// Input.js

import React from 'react';

function Input(props) {
  function handleChange(event) {
    props.onChange(event.target.value);
  }

  return (
    <input type="text" value={props.value} onChange={handleChange} />
  );
}

export default Input;
```

In this example, we're creating a simple function component called Input. The component takes a props object as an argument, which contains a value property that specifies the current value of the input field, and an onChange property that specifies the event handler function to call when the user changes the input value.

The handleChange function is defined within the Input component, and is called when the user changes the input value. The handleChange function calls the onChange function that was passed in as a prop, with the new value of the input field.

To use this component in another part of your code, you simply import it and use it like any other HTML tag. For example:

```js
// App.js

import React, { useState } from 'react';
import Input from './Input';

function App() {
  const [value, setValue] = useState('');

  function handleInputChange(newValue) {
    setValue(newValue);
  }

  return (
    <div>
      <Input value={value} onChange={handleInputChange} />
      <p>Current value: {value}</p>
    </div>
  );
}

export default App;
```

In this example, we're using the Input component to render an input field to the user. The component takes a value prop, which is set to the current value of the input field, and an onChange prop,


### 7.4. Tutorial
Our components can react to different events such as hover, click, form submission, keyboard, scroll events and more! This tutorial will focus on click events.ß

In the Home.js component we created a button element. When a user clicks this button, we want to execute a function. We create a function for handling this event like `handleClick`. This is a typical naming convention followed for such an event. Other events and their corresponding function names would be `handleMouseOver`, `handleSubmit` etc. In order to link the function to the button element, we need to configure the event listener. Here is where we declare `onClick={handleClick}`. You specifically do not invoke the function `handleClick()` because this will execute the function automatically, without the user even clicking on the button. Hence, we only have a reference to the function, so when the user clicks the button, the function will then (and only then) be invoked.

Home.js:
```js
import React from 'react'

const Home = () => {

    const handleClick = () => {
        alert('Hello!');
    }

  return (
    <div className="home">
        <h2>Homepage</h2>
        <button onClick={handleClick}>Click me</button>
    </div>
  )
}

export default Home
```

What if we want to pass in argument to the function, such as a name? What we would could do is pass in the name in parenthesis as such `onClick={handleClick('yoshi')}`, but this would automatically invoke this function right away. Instead, we have to wrap this inside of an anonymous function so it only triggers upon the event!

Home.js:
```js
import React from 'react'

const Home = () => {

    const handleClick = () => {
        alert('Hello!');
    }

    const handleClickAgain = (name) => {
        alert(`Hello ${name}!`);
    }

  return (
    <div className="home">
        <h2>Homepage</h2>
        <button onClick={handleClick}>Click me</button>
        <button onClick={() => handleClickAgain('yoshi')}>Click me again</button>
    </div>
  )
}

export default Home
```

Browser View:

![Section 6 Browser View](/images/section-6-browser-view.png)
![Section 6 Browser View Event 1](/images/section-6-browser-view-event-1.png)
![Section 6 Browser View Event 2](/images/section-6-browser-view-event-2.png)

When an event occurs, we have access to the 'event' object inside of these event handler functions. In this demonstration we will convert the above example to output the event object into the console also. This event object contains many properties which we can use in our app.

Home.js:
```js
import React from 'react'

const Home = () => {

    const handleClick = (e) => {
        console.log('Hello!', e)
    }

    const handleClickAgain = (name, e) => {
        console.log(`Hello ` + name, e.target);
    }

  return (
    <div className="home">
        <h2>Homepage</h2>
        <button onClick={handleClick}>Click me</button>
        <button onClick={(e) => handleClickAgain('yoshi', e)}>Click me again</button>
    </div>
  )
}

export default Home
```

Browser/Console View:

![Section 6 Console](/images/section-6-console.png)

## 8. Hooks

### 8.1. What are Hooks in ReactJS?
Hooks are a new feature introduced in ReactJS 16.8 that allow you to use state and other React features, without writing a class component. Hooks provide a way to use React's stateful features in functional components, which makes it easier to write and maintain your code.

There are several built-in hooks in ReactJS that allow you to manage state, effects, and more.

### 8.2. Why do we use Hooks?
Hooks are functions that let us “hook into” state and lifecycle functionality in function components.

Hooks allow us to:

- reuse stateful logic between components
- simplify and organize our code to separate concerns, rather than allowing unrelated data to get tangled up together
- avoid confusion around the behavior of the this keyword
- avoid class constructors, binding methods, and related advanced JavaScript techniques

### 8.3. Hook Rules

There are two main rules to keep in mind when using Hooks:
- Only call Hooks from React function components.
- Only call Hooks at the top level, to be sure that Hooks are called in the same order each time a component renders.

Common mistakes to avoid are calling Hooks inside of loops, conditions, or nested functions.


### 8.4. useState Hook

NOTE: This topic is a repeat of X. State above.

The useState hook allows you to add state to your functional components. Here's an example of how to use the useState hook:

```js
import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  function handleClick() {
    setCount(count + 1);
  }

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={handleClick}>Increment</button>
    </div>
  );
}

export default Counter;
```

In this example, we're creating a functional component called Counter. The component uses the useState hook to add state to the component. The state value is stored in the count variable, and the setCount function is used to update the state.

The handleClick function is called when the user clicks the button. It calls the setCount function to update the count state by incrementing it by 1.

NOTE: useState() may be called more than once in a component. This gives us the freedom to separate concerns, simplify our state setter logic, and organize our code in whatever way makes the most sense to us!

```js
function App() {
 const [sport, setSport] = useState('basketball');
 const [points, setPoints] = useState(31);
 const [hobbies, setHobbies] = useState([]);
}
```

Link to: Link to: [Full React Tutorial #8 - Using State (useState hook)](https://www.youtube.com/watch?v=4pO-HcG2igk&list=PL4cUxeGkcC9gZD-Tvwfod2gaISzfRiP9d&index=8)

### 8.5. useEffect Hook
The useEffect hook allows you to perform side effects, such as fetching data or updating the document title, in functional components. Here's an example of how to use the useEffect hook:

```js
import React, { useState, useEffect } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    document.title = `Count: ${count}`;
  }, [count]);

  function handleClick() {
    setCount(count + 1);
  }

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={handleClick}>Increment</button>
    </div>
  );
}

export default Counter;
```

In this example, we're using the useEffect hook to update the document title whenever the count state changes. The useEffect hook takes a function that performs the side effect, and an array of dependencies that determine when the side effect should be re-run.

In this case, we're passing the count variable as a dependency, so the effect will be re-run whenever the count state changes.

NOTE: By default, with no dependency array provided, our effect is called after every render. An empty dependency array signals that our effect will run after the initial render, and never needs to be re-run afterwards. A non-empty dependency array signals to the Effect Hook that it only needs to call our effect again when the value/state of one of the listed dependencies has changed. All 3 possibilities are demonstrated below.

```js
useEffect(() => {
 alert('called after every render');
});
 
useEffect(() => {
 alert('called after first render');
}, []);
 
useEffect(() => {
 alert('called when value of `endpoint` or `id` changes');
}, [endpoint, id]);
```

NOTE: useEffect() may be called more than once in a component. This gives us the freedom to individually configure our dependency arrays, separate concerns, and organize our code in whatever way makes the most sense to us. For example:

```js
function App(props) {
 const [title, setTitle] = useState('');
 useEffect(() => {
   document.title = title;
 }, [title]);
 
 const [time, setTime] = useState(0);
 useEffect(() => {
   const intervalId = setInterval(() => setTime((prev) => prev + 1), 1000);
   return () => clearInterval(intervalId);
 }, []);
  
 // ...
}
```

Link to: [Full React Tutorial #15 - useEffect Dependencies](https://www.youtube.com/watch?v=jQc_bTFZ5_I&list=PL4cUxeGkcC9gZD-Tvwfod2gaISzfRiP9d&index=16).

### 8.6. Custom Hooks
You can also create your own custom hooks to encapsulate complex stateful behavior and make it reusable across multiple components. Here's an example of how to create a custom hook:

```js
import { useState, useEffect } from 'react';

function useWindowWidth() {
  const [width, setWidth] = useState(window.innerWidth);

  useEffect(() => {
    function handleResize() {
      setWidth(window.innerWidth);
    }

    window.addEventListener('resize', handleResize);

    return () => {
      window.removeEventListener('resize', handleResize);
    };
  }, []);

  return width;
}

export default useWindowWidth;
```

In this example, we're creating a custom hook called useWindowWidth that tracks the width of the browser window. The hook uses the useState hook to add state to the component, and the useEffect hook to update the state whenever the window is resized.

The hook returns the current width of the window, which can be used in any functional component that imports the useWindowWidth hook.

To use this hook in another component, you simply import it and call it like any other hook. For example:

```js
import React from 'react';
import useWindowWidth from './useWindowWidth';

function MyComponent
```

### 8.7. Tutorial
#### 8.7.1. Outputting Lists

As we are developing a blog website, we need a list of blogs stored in an array. We will be using the useState hook to create the data, as if it changes, its state will need updating. For example, if we delete a blog we need React to update the DOM accordingly and output the new list of blogs with the deleted blog removed. The list requires each item to have a unique id. This will be used by React to output the list of data.

We need a template for each item. We could hard code this by adding 3 div's and their respective elements (such as h1's and such). But, this is not ideal. It is time consuming, repeating code and the data may change at some point. For example, if we add more blogs in the future then we will have to manually add these in the source code. Or, if we delete some blogs, it will not update automatically and would require the same manual changes to remove the blogs. 

Instead, we want to cycle through the array using JavaScript and output a template for each item. This way, it will not matter if there are 3 blogs.. or 100! Here we will use the map() method. The array method map() comes up often in React. It’s good to get in the habit of using it alongside JSX. A common use of this method is for creating a list of JSX elements from a given array. Simply map() over each element in the array and return a template we want to render for each item in the array.

When we output a list using the map method, each root element in the template that we return must have a key property. The key attribute is used to uniquely identify individual elements. It is declared like any other attribute. If data changes at any point (added or removed) then React can keep track of these items. Keys can help performance because they allow React to keep track of whether individual list items should be rendered or if the order of individual items is important.

In React, JSX attribute values can be set through data stored in regular JavaScript objects. We see this in the example block of code. In our code example we first see our JavaScript object blogs and the values stored with these items. We then see how these stored values are used to set the div attribute 'key' in our JSX expression for the Home component.

Home.js:
```js
import React from 'react'
import { useState } from 'react';

const Home = () => {

   const [blogs, setBlogs] = useState([
    { title: 'My new website', body: 'lorem ipsum...', author: 'mario', id: 1},
    { title: 'Welcome party!', body: 'lorem ipsum...', author: 'yoshi', id: 2},
    { title: 'Web dev top tips', body: 'lorem ipsum...', author: 'mario', id: 3}
   ]);
    
  return (
    <div className="home">
        {blogs.map((blog) => (
            <div className="blog-preview" key={blog.id}>
                <h2>{ blog.title }</h2>
                <p>Written by {blog.author}</p>
            </div>
        ))}
    </div>
  )
}

export default Home
```

Browser View:

![Section 9 List](/images/section-9-list.png)

Note: CSS styling has been added to the items.

#### 8.7.2. Using JSON Server

useEffect is a great way to fetch data in a component because it runs the function when the component first renders initially. This is when we want to fetch some data. We can use this data in our app instead of the hardcoded data (blogs) we stored initially. The Data comes from the database which is accessed via an API endpoint. To create the database and REST API we could use ExpressJS. But for the purposes of this frontend UI ReactJS project, we can use JSON Server instead.

JSON Server is a package to help build a dummy REST API using a JSON file so we can test the functionality of our frontend code. First create a JSON file that acts as our database. Here, we will create a folder called 'data' with a file named 'db.json'. We can now add the blogs (as a property), which contains an array of 2 blog objects. JSON Server will see blogs at the top level and creates n endpoint for blogs so we can interact with the resource. Now, we can perform CRUD operations on the property blogs. 

As we need to use the JSON Server package, we must first configure the package. In a new terminal, run command `npx json-server --watch data/db.json --port 8000`.

This command makes the JSON Server generate the endpoints based on the data it is watching in the 'db.json' file on port 8000.

![JSON Server Endpoints](/images/json-server-endpoints.png)

#### 8.7.3. Fetching Data in useEffect

We initialize the state of blogs as empty so: useState(null). Then we use useEffect to fetch the blog data on first render. We will do this via the fetch API. The code snippet below explains the fetch call structure and how it works.

 ```js
fetch(url) // asynchronously load contents of the url
           // return a Promise that resolves when res is loaded
      .then(res => res.json()) // call this function when res is loaded
      // return a Promise with result of above function
      .then(res => { // call this function when the above chained Promise resolves
        this.setState({
          data: res,
          error: res.error || null,
          loading: false
        });
 ```

NOTE: In JavaScript, the fetch() method is used to make asynchronous requests to the server and load the information that is returned by the server onto the web pages.

#### 8.7.4. JSX Conditionals
JSX does not support if/else syntax in embedded JavaScript. There are three ways to express conditionals for use with JSX elements:

- a ternary within curly braces in JSX
- an if statement outside a JSX element
- the && operator

In JSX, && is commonly used to render an element based on a boolean condition. && works best in conditionals that will sometimes do an action, but other times do nothing at all.

If the expression on the left of the && evaluates as true, then the JSX on the right of the && will be rendered. If the first expression is false, however, then the JSX to the right of the && will be ignored and not rendered. All 3 possibilities are demonstrated below.

```js
// Using ternary operator
const headline = (
  <h1>
    { age >= drinkingAge ? 'Buy Drink' : 'Do Teen Stuff' }
  </h1>
);

// Using if/else outside of JSX 
let text;

if (age >= drinkingAge) { 
    text = 'Buy Drink' 
  } else { 
    text = 'Do Teen Stuff' 
}

const headline = <h1>{ text }</h1>

// Using && operator. Renders as empty div if length is 0
const unreadMessages = [ 'hello?', 'remember me!'];

const update = (
  <div>
    {unreadMessages.length > 0 &&
      <h1>
        You have {unreadMessages.length} unread messages.
      </h1>
    }
  </div>
);
```

Home.js:
```js
import React from 'react'
import { useState, useEffect } from 'react';
import BlogList from './BlogList';

const Home = () => {

   const [blogs, setBlogs] = useState(null);

   const handleDelete = (id) => {
      const newBlogs = blogs.filter((blog) => blog.id !== id);
      setBlogs(newBlogs);
   }

   useEffect(() => {
    fetch('http://localhost:8000/blogs')
    .then(res => {
      return res.json();
    })
    .then((data) => {
      setBlogs(data)
    })
   }, []);
    
  return (
    <div className="home">
        {blogs && <BlogList blogs={blogs} title="All Blogs!" handleDelete={handleDelete}/>}
    </div>
  )
}

export default Home
```

Browser View:
![useEffect fetch](/images/section-17-use-effect-fetch.png)

#### 8.7.5. Conditional Loading Message

It would be ideal to create a loading message whilst the user is waiting for the data that is being fetched. This will indicate to the user that their request is being processed. Our fetch is very quick as the application is being run locally, but in production, the fetch will be over the internet to a server which will take more time.

Here we add an 'isLoading' State Hook and set it to true by default. We update the useEffect Hook to setIsLoading to false once the blog data has been fetched and assigned. In the JSX, we add a conditional template that renders a "Loading..." div when isLoading is true!

Home.js:
```js
import React from 'react'
import { useState, useEffect } from 'react';
import BlogList from './BlogList';

const Home = () => {

   const [blogs, setBlogs] = useState(null);
   const [isLoading, setIsLoading] = useState(true);

   const handleDelete = (id) => {
      const newBlogs = blogs.filter((blog) => blog.id !== id);
      setBlogs(newBlogs);
   }

   useEffect(() => {
    fetch('http://localhost:8000/blogs')
    .then(res => {
      return res.json();
    })
    .then((data) => {
      setBlogs(data)
      setIsLoading(false)
    })
   }, []);
    
  return (
    <div className="home">
        {isLoading && <div>Loading...</div>}
        {blogs && <BlogList blogs={blogs} title="All Blogs!" handleDelete={handleDelete}/>}
    </div>
  )
}

export default Home
```

#### 8.7.6. Handling Fetch Errors

We should handle any errors from the fetch request we made earlier & output any errors in the template. This could be an error sent back from the server, or a connection error where the client cannot connect to the server. We need to let the user know that there will be no data retrieved and there is some kind of error. We need to add a catch block at the end of the fetch request. This catches any network error (connection error) and executes a function.

What about if there is another type of error? For example, if the request reaches the server... but the server sends an error back if the endpoint that is faulty, or does not exist, or the request is denied. This catch block will not capture this error, because technically the request is still reaching the server, and the server is still sending a response object back to us.. it is just the response object sent back contains no data, just a different status (4xx or 5xx).

4xx client error – the request contains bad syntax or cannot be fulfilled. 5xx server error – the server failed to fulfil an apparently valid request.

So we need to perform an if check for server response errors. The response object has a property called ok. res.ok returns a boolean value, true if the response is okay (2xx), false otherwise. So, if the response is not ok (!res.ok), then we want to throw an error!

If we change the URL to an endpoint that does not exist (/blogss), then make a request to server, the server will respond with an error and we will catch it, throw our error, and send a message.

We want to store the error in a state, so we can output it to the browser. We useState for the error and if we catch an error, we setError as the error message. By default its state is set to null. We add conditional rendering again, if there is an error, we output the error in a div.

NOTE: We setIsLoading as false as we do not display a loading message in the event of an error, we only want to display the error message alone. 

NOTE: We setError as null if we get data. The reason for this is if we try to fetch the data again, making a subsequent request at any point, we want to remove that error message if it is successful. This is done by resetting the state of error to remove any previous error messages.

Home.js:
```js
import React from 'react'
import { useState, useEffect } from 'react';
import BlogList from './BlogList';

const Home = () => {

   const [blogs, setBlogs] = useState(null);
   const [isLoading, setIsLoading] = useState(true);
   const [error, setError] = useState(null);

   const handleDelete = (id) => {
      const newBlogs = blogs.filter((blog) => blog.id !== id);
      setBlogs(newBlogs);
   }

   useEffect(() => {
    fetch('http://localhost:8000/blogs')
    .then(res => {
      if (!res.ok) {
        throw Error('Could not fetch the data for that resource')
      }
      return res.json()
    })
    .then((data) => {
      setError(null);
      setBlogs(data)
      setIsLoading(false)
    })
    .catch(err => {
      setError(err.message);
      setIsLoading(false);
    })
   }, []);
    
  return (
    <div className="home">
        {error && <div>{ error }</div>}
        {isLoading && <div>Loading...</div>}
        {blogs && <BlogList blogs={blogs} title="All Blogs!" handleDelete={handleDelete}/>}
    </div>
  )
}

export default Home
```

#### 8.7.7. Making a Custom Hook

Now we have all of this logic in the useEffect Hook. All of the state properties. Everything is working fine and it is okay to be left as such:

Home.js:
```js
import React from 'react'
import { useState, useEffect } from 'react';
import BlogList from './BlogList';

const Home = () => {

   const [blogs, setBlogs] = useState(null);
   const [isLoading, setIsLoading] = useState(true);
   const [error, setError] = useState(null);

   const handleDelete = (id) => {
      const newBlogs = blogs.filter((blog) => blog.id !== id);
      setBlogs(newBlogs);
   }

   useEffect(() => {
    fetch('http://localhost:8000/blogs')
    .then(res => {
      if (!res.ok) {
        throw Error('Could not fetch the data for that resource')
      }
      return res.json()
    })
    .then((data) => {
      setError(null);
      setBlogs(data)
      setIsLoading(false)
    })
    .catch(err => {
      setError(err.message);
      setIsLoading(false);
    })
   }, []);
    
  return (
    <div className="home">
        {error && <div>{ error }</div>}
        {isLoading && <div>Loading...</div>}
        {blogs && <BlogList blogs={blogs} title="All Blogs!" handleDelete={handleDelete}/>}
    </div>
  )
}

export default Home
```

But, what if we want to do a similar type of action in another component in the future. The operation being carried out is fetching of data where the data, loading message and errors are being displayed (if any). This task itself is very useful but we do not want to rewrite all of this whenever we want to carry out this task. It is not efficient or easy to manage. This is where custom hooks come in. This way we are only writing and maintaining the logic in one place. We are externalizing the logic into its own file. This custom hooks ability will be to fetch data.

First we make a new file (useFetch.js) in src folder. Custom hooks in react must begin with 'use'. Make a functional component. Inside this file we cut and paste all of the functionality that was written (including the useEffect) from the Home component. We now need to make some adjustments. We need to import useEffect and register all of the states. They are still in the Home component, but we must move it to the custom hook location as we are no longer setting those states in Home.js. We must now import useState also. To generalize the logic and make it more reusable, we change the 'blogs' to 'data'. Because in the future when using the useFetch hook, we could be fetching a different type of resource, such as tags or categories, so it does not make sense to leave it as blogs.

Similar to how when calling useState returns some values, we can do the same for our custom hooks! We will return an object for whenever useFetch is called.

Note: Can also return an array (like useState) or anything. We use objects because the order of the properties does not matter when destructuring them, and we can grab just any number of properties without the others if we so desired.

We also want to make one more change. We want to pass the 'url' as an argument, as opposed to hardcoding it. This is so we can use the hook with any url endpoint resource we are trying to fetch data from. We pass url as an argument to useFetch and place the url as a dependency (in the dependency array) to useEffect. This means whenever the url changes, it is going to re-run the useEffect function to get the data for that particular endpoint.

Finally, we need to import this useFetch function into the Home component and implement it. We want to destruct the 3 properties. Notice that there is an error, we are using 'blogs' in the return but we have declared 'data' above. We can either rename blogs in the return as data OR we can name the data blogs in the component by writing `data: blogs` which grabs the data but calls it blogs in the context of this component.


useFetch.js:
```js
import { useState, useEffect } from 'react';

const useFetch = (url) => {
   const [data, setData] = useState(null);
   const [isLoading, setIsLoading] = useState(true);
   const [error, setError] = useState(null);

   useEffect(() => {
    fetch(url)
    .then(res => {
      if (!res.ok) {
        throw Error('Could not fetch the data for that resource')
      }
      return res.json()
    })
    .then((data) => {
      setError(null);
      setData(data)
      setIsLoading(false)
    })
    .catch(err => {
      setError(err.message);
      setIsLoading(false);
    })
   }, [url]);

   return { data, isLoading, error }
}

export default useFetch;
```

Home.js:
```js
import React from 'react'
import BlogList from './BlogList';
import useFetch from './useFetch';

const Home = () => {

  const {data: blogs, isLoading, error } = useFetch('http://localhost:8000/blogs');
 
  return (
    <div className="home">
        {error && <div>{ error }</div>}
        {isLoading && <div>Loading...</div>}
        {blogs && <BlogList blogs={blogs} title="All Blogs!"/>}
    </div>
  )
}

export default Home
```

#### 8.7.8. useEffect Cleanup
What is the useEffect cleanup function? It is a function of the useEffect hook that allows us to stop side effects that no longer need to be executed before our component is unmounted. useEffect is built in such a way that we can return a function inside it and this return function is where the cleanup happens. 

React's useEffect cleanup function saves applications from unwanted behaviors like memory leaks by cleaning up effects. In doing so, we can optimize our application's performance

There are different ways to cancel fetch request calls, we can use fetch AbortController or Axios AbortController.

Firstly we create an AbortController which we can associate with a specific fetch request. Here, we can use it to stop the fetch. To associate it with a fetch we add a second argument to fetch, and set the 'signal' property to `abortController.signal`. We can now use this to stop that fetch. We do this inside the return cleanup, where we set the callback function equal to `abortController.abort()`. As we are aborting a fetch, the fetch will throw an error. When we get an error, the catch block is run and updates the state, despite not retrieving the data anymore. We need to add an if condition block in the catch block to prevent updating the state when an 'abort error' is caught. If it is a specific type of error, an abort error, then we do not want to update the state. If it is any other type of error, we update the state.

useFetch.js:
```js
import { useState, useEffect } from 'react';

const useFetch = (url) => {
   const [data, setData] = useState(null);
   const [isLoading, setIsLoading] = useState(true);
   const [error, setError] = useState(null);

   useEffect(() => {

    const abortController = new AbortController();

    fetch(url, { signal: abortController.signal })
    .then(res => {
      if (!res.ok) {
        throw Error('Could not fetch the data for that resource')
      }
      return res.json()
    })
    .then((data) => {
      setError(null);
      setData(data)
      setIsLoading(false)
    })
    .catch(err => {
        if (err.name === 'AbortError') {
            console.log('fetch aborted');
        } else {
            setError(err.message);
            setIsLoading(false);
        }
    })

    return () => abortController.abort();
   }, [url]);

   return { data, isLoading, error }
}

export default useFetch;
```

More info: [Cleanup Functions in React’s UseEffect Hook](https://hackernoon.com/cleanup-functions-in-reacts-useeffect-hook-explained)

#### 8.7.9. Re-using a Custom Hook
Now that we have the BlogList component page setup, we need to fetch the data for that blogs id. For this, we will reuse the custom hook we created, useFetch(). We can use the id to make a fetch request for that particular blog, within the BlogDetails component, by calling the useFetch() hook. First we use the fetch hook with the blogs url & id and destructure our 3 properties, data (renamed as blog), isLoading and error. Then in the return statement for the JSX template, we use the { var && JSX} format for conditional rendering depending on the value of our properties. We finally add some CSS styles of our liking to change the appearance of the content on the BlogDetails page.

NOTE: useParams returns an object of the Route parameters. This means we can deconstruct the id with { id } = useParams() to grab the id of the path and use the id param to dynamically fetch data from the api.

BlogDetails.js:
```js
import React from 'react'
import { useParams } from 'react-router-dom'
import useFetch from './useFetch';

const BlogDetails = () => {
    const { id } = useParams();

    const { data: blog, error, isLoading} = useFetch('http://localhost:8000/blogs/' + id);

  return (
    <div className="blog-details">
        { isLoading && <div>Loading...</div>}
        { error && <div> {error} </div>}
        { blog && (
            <article>
                <h2>{ blog.title }</h2>
                <p> Written by { blog.author }</p>
                <div>{ blog.body }</div>
            </article>
        )}
    </div>
  )
}

export default BlogDetails
```

index.css:
```css
/* blog details page */
.blog-details h2 {
  font-size: 20px;
  color: #f1356d;
  margin-bottom: 10px;
}
.blog-details div {
  margin: 20px 0;
}
```


## 9. Lifecycle Methods

<b>NOTE OPEN</b>

The primary purpose of a React component is to return some JSX to be rendered. Often, it is helpful for a component to execute some code that performs side effects in addition to rendering JSX.

In class components, side effects are managed with lifecycle methods. In function components, we manage side effects with the Effect Hook. Some common side effects include: fetching data from a server, subscribing to a data stream, logging values to the console, interval timers, and directly interacting with the DOM.

For the purpose of learning, this section will explain lifecycle methods in class components, but note that modern React apps tend towards function components which manage side effects with the Effect Hook.

<b>NOTE CLOSE</b>

ReactJS components have a lifecycle that goes through different stages as the component is created, updated, and destroyed. The lifecycle methods allow you to hook into these stages and perform actions at different points in the component's lifecycle.

There are three main phases in a React component's lifecycle:

1. Mounting: When a component is first created and added to the DOM.
2. Updating: When a component's props or state change and the component needs to be re-rendered.
3. Unmounting: When a component is removed from the DOM.

Each phase has its own set of lifecycle methods that you can use to hook into that phase of the component's lifecycle.

### 9.1. Mounting Phase
The mounting phase occurs when a component is first created and added to the DOM. The following lifecycle methods are called during the mounting phase:

1. constructor(): This method is called when the component is first created. You can use it to initialize state and bind event handlers.
2. static getDerivedStateFromProps(): This method is called after the constructor and before the render method. It allows you to update the state based on changes to the props.
3. render(): This method is called to generate the HTML for the component.
4. componentDidMount(): This method is called after the component is added to the DOM. You can use it to fetch data from an API or set up event listeners.

### 9.2. Updating Phase
The updating phase occurs when a component's props or state change and the component needs to be re-rendered. The following lifecycle methods are called during the updating phase:

1. static getDerivedStateFromProps(): This method is called before the render method. It allows you to update the state based on changes to the props.
2. shouldComponentUpdate(): This method is called before the component is re-rendered. You can use it to determine whether or not the component should be re-rendered.
3. render(): This method is called to generate the HTML for the component.
4. getSnapshotBeforeUpdate(): This method is called after the render method but before the changes are applied to the DOM. You can use it to get information about the component's state or props before the update.
5. componentDidUpdate(): This method is called after the changes have been applied to the DOM. You can use it to update the component's state or fetch new data.

### 9.3. Unmounting Phase
The unmounting phase occurs when a component is removed from the DOM. The following lifecycle method is called during the unmounting phase:

1. componentWillUnmount(): This method is called before the component is removed from the DOM. You can use it to clean up any event listeners or other resources that the component has created.

### 9.4. Tutorial
Here's an example of how you might use the componentDidMount lifecycle method to fetch data from an API:

```js
import React, { Component } from 'react';

class MyComponent extends Component {
  constructor(props) {
    super(props);
    this.state = {
      data: []
    };
  }

  componentDidMount() {
    fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(data => {
        this.setState({ data });
      });
  }

  render() {
    return (
      <div>
        {this.state.data.map(item => (
          <div key={item.id}>{item.name}</div>
        ))}
      </div>
    );
  }
}

export default MyComponent;
```

In this example, we're using the componentDidMount lifecycle method to fetch data from an API and update the component's state with the data. The render method then displays the data on the page.

## 10. React Router
React Router is a popular library for handling routing in React applications. It allows you to define routes in your application and map them to different components.

To get started with React Router, you'll need to install it using npm:
```bash
npm install react-router-dom
```

Once you've installed React Router, you can import it in your application:
```js
import { BrowserRouter, Route, Switch } from 'react-router-dom';
```

Let's say you have a simple React application with two components: Home and About. You want to set up routes so that when the user navigates to the root URL of your application, the Home component is displayed, and when they navigate to "/about", the About component is displayed.

Here's how you can set up those routes using React Router:
```js
import React from 'react';
import { BrowserRouter, Route, Switch } from 'react-router-dom';
import Home from './Home';
import About from './About';

function App() {
  return (
    <BrowserRouter>
      <Switch>
        <Route exact path="/" component={Home} />
        <Route path="/about" component={About} />
      </Switch>
    </BrowserRouter>
  );
}

export default App;
```

In this example, we're importing the BrowserRouter, Route, and Switch components from React Router. We're also importing the Home and About components that we want to display.

We're wrapping our routes in a BrowserRouter component, which provides the navigation functionality. The Switch component ensures that only one route is matched at a time.

We're defining two routes: one for the root URL of our application (exact path="/"), and one for "/about". We're mapping each of these routes to the appropriate component using the component prop.

Now, when the user navigates to the root URL of your application, the Home component will be displayed, and when they navigate to "/about", the About component will be displayed.

You can also pass props to your components through the Route component. Here's an example:

```js
<Route
  exact
  path="/"
  render={(props) => <Home {...props} greeting="Hello" />}
/>
```

In this example, we're passing the prop "greeting" with the value "Hello" to the Home component using the render prop.

React Router also provides a number of other features, such as URL parameters and nested routes. You can find more information in the React Router documentation.

### 10.1. Tutorial
#### 10.1.1. The React Router
Most websites have more than 1 page. So to introduce multiple pages (or routes) we use the React Router. Typical multi-page websites (that do not use React) send requests to the server for each page that is being visited. The server responds with the web pages html. React websites do not work in this manner. They delegate all the routing and changing of page content to the browser only. They start the same way, making an initial request in the browser, the server responds by the html page (index.html) back to the browser, but it also sends back our compiled ReactJS files. So from this point on, React and the React router can take control of the application. React injects the page dynamically. If we want to access a different route, react intercepts the call and updates the DOM with the corresponding components.

This entire process means we are making less requests to the server, and the website therefore feels faster.

Firstly, we must install the React Router package as it is not part of react library package.

Run `npm install react-router-dom` command in a new terminal. Once installed, you will see react-router-dom package in package.json (and in node_modules).

In App.js we import 3 properties from React Router library. BrowserRouter, Route, Switch. We surround the entire app with the Router component, so that we can use Router in the entire app now. All components nested inside the Router component now have access to the router. All of our routes go inside the Switch component. We nest each component in a Route component to setup each page. We purposely do not place the NavBar in the Switch component, or in a Route component, because we want it to be present for every route.

Also, let's create a new component Create.js that will be a page to fill out a web form, which creates a new blog upon submission. We add a new Route 'Create' to App.js. We need to add 'exact path' as the exact param disables the partial matching for a route, and makes sure that it only returns the route if the path is an EXACT match to the current url. 

NOTE: Now with React Router V6 we don't need this prop anymore because React Router will always look for the exact path we pass. 

Source: [Changes to React Router after v6](https://dev.to/gabrlcj/react-router-v6-some-of-the-new-changes-181m)

One more change we need to make is the anchor tags in our NavBar component. If we want React to handle the routing only within the browser and intercept requests made to the server, we need to import and use Link components instead of anchor tags. These still behave like anchor tags, but the only difference is it has built in functionality for React Router to have the ability to prevent these requests to the server and instead, it just looks at the URL/path and matches that against one of the Route components. This change makes clicking on links to new pages and loading these pages extremely fast!

Create.js:
```js
const Create = () => {
  return (
    <div className="create">
        <h2>Add a New Blog</h2>
    </div>
  );
}

export default Create;
```

NavBar.js:
```js
import { Link } from 'react-router-dom';

const Navbar = () => {
  return (
    <nav className='navbar'>
        <h1>The Arsalaan Blog</h1>
        <div className="links">
            <Link to="/">Home</Link>
            <Link to="/create">New Blog</Link>
        </div>
    </nav>
  )
}

export default Navbar
```

App.js:
```js
import Navbar from './Navbar';
import Home from './Home';
import { BrowserRouter as Router, Route, Routes} from 'react-router-dom';
import Create from './Create';

const App = () => {
  return (
    <Router>
      <div className="App">
        <Navbar />
        <div className="content">
          <Routes>
            <Route path="/" element={<Home />} />
            <Route path='/create' element={<Create />} />
          </Routes>
        </div>
      </div>
    </Router>
  );
}

export default App;
```

#### 10.1.2. Route Parameters
Sometimes we need to pass dynamic values as part of a route. For example, /blogs/1 or /blogs/12, for a blog details page where 1 and 12 are the id's of the blogs we want to see. This changeable part in the route is like a variable, it is a route parameter. In our react app we need to use and access these route parameters so in our components, we can use these id's to fetch data for that particular blog. 

We create the BlogDetails component. Add a Route in the App component to this new page. To add a changeable parameter in the path attribute of Route, write as such: '/blogs/:id'. We still need to add the logic/functionality for fetching the details. We use a hook for this. The useParams() hook allows us to grab the route parameters, we need to just add this to the destructure. On the Home component, we need to add links to the blogs list, so if a user clicks on any blog, it redirects them to that blogs details route to the id of that clicked blog. So, we add a Link tag and surround the h2 and p tags. We do not hardcode the path, we want it to be dynamic. We finally add some CSS styles of our liking to change the appearance of the Link tag on the BlogList component.

App.js:
```js
import Navbar from './Navbar';
import Home from './Home';
import { BrowserRouter as Router, Route, Routes} from 'react-router-dom';
import Create from './Create';
import BlogDetails from './BlogDetails';

const App = () => {
  return (
    <Router>
      <div className="App">
        <Navbar />
        <div className="content">
          <Routes>
            <Route path="/" element={<Home />} />
            <Route path='/create' element={<Create />} />
            <Route path='/blogs/:id' element={<BlogDetails />} />
          </Routes>
        </div>
      </div>
    </Router>
  );
}

export default App;
```

BlogDetails.js:
```js
import React from 'react'
import { useParams } from 'react-router-dom'

const BlogDetails = () => {
  const { id } = useParams();

  return (
    <div className="blog-details">
        <h2>Blog details - { id }</h2>
    </div>
  )
}

export default BlogDetails
```

BlogList.js:
```js
import React from 'react'
import { Link } from 'react-router-dom'

const BlogList = ({ blogs, title, handleDelete }) => {
  return (
    <div className="blog-list">
        <h2>{ title }</h2>
        {blogs.map((blog) => (
            <div className="blog-preview" key={blog.id}>
                <Link to={`/blogs/${blog.id}`}>
                <h2>{ blog.title }</h2>
                <p>Written by {blog.author}</p>
                </Link>
            </div>
        ))}
    </div>
  )
}

export default BlogList
```

index.css:
```css
.blog-preview a {
    text-decoration: none;
  }
```

## 11. Web Forms
### 11.1. Tutorial
#### 11.1.1. Controlled Inputs

Now we will look at web forms. We want a user to be able to add a new blog and submit it, then a post request should be sent so the new blog is added to the current list of blogs data. Lets create a template for the form in the Create.js component. Lets add some CSS styles to improve the UI. We need to track the values on the form and store them in some state. 

useState('') will set the field empty but when we try to type in the box, it does not change and remains ''. We need to set the state within the input label so it will update the state if a different value is entered. We need the 'value' and 'onChange' properties for the fields. The onChange function callback will always follow the same format, where 'e' is the event object.

Next we will learn how to submit the form.

index.css:
```js
/* create new blog form */
.create {
  max-width: 400px;
  margin: 0 auto;
  text-align: center;
}
.create label {
  text-align: left;
  display: block;
}
.create h2 {
  font-size: 20px;
  color: #f1356d;
  margin-bottom: 30px;
}
.create input, .create textarea, .create select {
  width: 100%;
  padding: 6px 10px;
  margin: 10px 0;
  border: 1px solid #ddd;
  box-sizing: border-box;
  display: block;
}
.create button {
  background: #f1356d;
  color: #fff;
  border: 0;
  padding: 8px;
  border-radius: 8px;
  cursor: pointer;
}
```

Create.js:
```js
import { useState } from "react";

const Create = () => {
  const [title, setTitle] = useState('');
  const [body, setBody] = useState('');
  const [author, setAuthor] = useState('mario');


  return (
    <div className="create">
        <h2>Add a New Blog</h2>
        <form>
            <label>Blog title:</label>
            <input 
                type="text" 
                required
                value={title}
                onChange={(e) => setTitle(e.target.value)}
            />
            <label>Blog body:</label>
            <textarea 
                required
                value={body}
                onChange={(e) => setBody(e.target.value)}
            />
            <label>Blog author:</label>
            <select
              value={author}
              onChange={(e) => setAuthor(e.target.value)}
            >
                <option value="mario">mario</option>
                <option value="yoshi">yoshi</option>
            </select>
            <button>Add Blog</button>
            <p>{ title }</p>
            <p>{ body } </p>
            <p>{ author } </p>
        </form>
    </div>
  );
}

export default Create;
```

#### 11.1.2. Submit Events

Now we want to handle the form being submitted. We can add a click event to the button and react to that. But another way to do it is to react to the submit event. In the form tag we add onSubmit={} and we create a handleSubmit event listener function. Firstly, we want to prevent the default action of the submit, which is to refresh the page. To prevent this, we use the method preventDefault() on the event object. Next, we want to create a blog object, which is the data that will be saved to the JSON server. The JSON server automatically generates an id for post requests, so we not need to add this ourselves.

The code below will cause the blog to be logged to the console upon submission, without the page refreshing.

Create.js:
```js
import { useState } from "react";

const Create = () => {
  const [title, setTitle] = useState('');
  const [body, setBody] = useState('');
  const [author, setAuthor] = useState('mario');

  const handleSubmit = (e) => {
    e.preventDefault();
    const blog = { title, body, author };

    console.log(blog)
  }

  return (
    <div className="create">
        <h2>Add a New Blog</h2>
        <form onSubmit={handleSubmit}>
            <label>Blog title:</label>
            <input 
                type="text" 
                required
                value={title}
                onChange={(e) => setTitle(e.target.value)}
            />
            <label>Blog body:</label>
            <textarea 
                required
                value={body}
                onChange={(e) => setBody(e.target.value)}
            />
            <label>Blog author:</label>
            <select
              value={author}
              onChange={(e) => setAuthor(e.target.value)}
            >
                <option value="mario">mario</option>
                <option value="yoshi">yoshi</option>
            </select>
            <button>Add Blog</button>
            <p>{ title }</p>
            <p>{ body } </p>
            <p>{ author } </p>
        </form>
    </div>
  );
}

export default Create;
```

#### 11.1.3. Sending POST Requests

Now we can submit the form and create the blog objects. The next step is to make a POST req to the JSON server to add the data to our data file. We could edit the useFetch hook so it can handle POST requests as well, thus making it more a universal hook. But instead, we are going to make the POST request inside the handleSubmit function as we are only going to make that request once in the entire app, not in two different places.

In the handleSubmit, we make a fetch call. The first argument is the route and the second argument is related to the request, this includes the method type, headers and the body (data) itself. We have to convert the object to a JSON string so we use a method to do us. JSON server will add the id for us. Since the call is async and it returns a Promise, we can attach a then() method, which fires a function when the request is complete. We have also added a loading state to the button while the request is being made. We use the useState hook with isLoading. We change the state of this property depending on which part of the handleSubmit request it is in. At the bottom, we add in the return the JSX to output two different types of buttons depending on the status of isLoading. This lets us know when we submit the form, when the data has successfully been sent.

NOTE: setTimeout() added just to see the isLoading functionality. We would not add this into our production code, only done for development and testing purposes so we have a chance to capture this feature that should be present when loading. In dev, response times are too quick for us to capture, but in prod we would be able to notice it.

Create.js:
```js
import { useState } from "react";

const Create = () => {
  const [title, setTitle] = useState('');
  const [body, setBody] = useState('');
  const [author, setAuthor] = useState('mario');
  const [isLoading, setIsLoading] = useState(false);

  const handleSubmit = (e) => {
    e.preventDefault();
    const blog = { title, body, author };

    setIsLoading(true);

    fetch('http://localhost:8000/blogs', {
        method: 'POST',
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify(blog)
    })
    .then(() => {
        setTimeout(() => {
            console.log('new blog added')
            setIsLoading(false)
        }, 1000);
    })
  }

  return (
    <div className="create">
        <h2>Add a New Blog</h2>
        <form onSubmit={handleSubmit}>
            <label>Blog title:</label>
            <input 
                type="text" 
                required
                value={title}
                onChange={(e) => setTitle(e.target.value)}
            />
            <label>Blog body:</label>
            <textarea 
                required
                value={body}
                onChange={(e) => setBody(e.target.value)}
            />
            <label>Blog author:</label>
            <select
              value={author}
              onChange={(e) => setAuthor(e.target.value)}
            >
                <option value="mario">mario</option>
                <option value="yoshi">yoshi</option>
            </select>
            { isLoading? <button disabled>Adding Blog...</button> : <button>Add Blog</button> }
        </form>
    </div>
  );
}

export default Create;
```

#### 11.1.4. Programmatic Redirects

It would be nice if we could redirect the user to the home page once the blog has been added. In order to do this, we can use another Hook called useHistory from the React Router package. This allows us to go back and forward through the history (like browser arrows) and also add a new page onto the history (redirect them to a new route). We just have to add a history object with useHistory(), then in the then() method, use the push() method with the home route '/' to redirect the user to the home page after the post request is complete.

User submits form, blog is added, once it is added, user is redirected to home page.

Create.js:
```js
import { useState } from "react";
import { useHistory } from "react-router-dom";

const Create = () => {
  const [title, setTitle] = useState('');
  const [body, setBody] = useState('');
  const [author, setAuthor] = useState('mario');
  const [isLoading, setIsLoading] = useState(false);
  const history = useHistory();

  const handleSubmit = (e) => {
    e.preventDefault();
    const blog = { title, body, author };

    setIsLoading(true);

    fetch('http://localhost:8000/blogs', {
        method: 'POST',
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify(blog)
    })
    .then(() => {
        setTimeout(() => {
            console.log('new blog added')
            setIsLoading(false)
            history.push('/')
        }, 1000);
    })
  }

  return (
    <div className="create">
        <h2>Add a New Blog</h2>
        <form onSubmit={handleSubmit}>
            <label>Blog title:</label>
            <input 
                type="text" 
                required
                value={title}
                onChange={(e) => setTitle(e.target.value)}
            />
            <label>Blog body:</label>
            <textarea 
                required
                value={body}
                onChange={(e) => setBody(e.target.value)}
            />
            <label>Blog author:</label>
            <select
              value={author}
              onChange={(e) => setAuthor(e.target.value)}
            >
                <option value="mario">mario</option>
                <option value="yoshi">yoshi</option>
            </select>
            { isLoading? <button disabled>Adding Blog...</button> : <button>Add Blog</button> }
        </form>
    </div>
  );
}

export default Create;
```

NOTE: There is no longer { useHistory } hook in react-router-dom v6. There is better a way to do the work of useHistory.

First import useNavigate and and follow the example below:

Create.js
```js
import { useState } from "react";
import { useNavigate } from "react-router-dom";


const Create = () => {
  const [title, setTitle] = useState('');
  const [body, setBody] = useState('');
  const [author, setAuthor] = useState('mario');
  const [isLoading, setIsLoading] = useState(false);
  const history = useNavigate();

  const handleSubmit = (e) => {
    e.preventDefault();
    const blog = { title, body, author };

    setIsLoading(true);

    fetch('http://localhost:8000/blogs', {
        method: 'POST',
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify(blog)
    })
    .then(() => {
        setTimeout(() => {
            console.log('new blog added')
            setIsLoading(false)
            history('/')
        }, 1000);
    })
  }

  return (
    <div className="create">
        <h2>Add a New Blog</h2>
        <form onSubmit={handleSubmit}>
            <label>Blog title:</label>
            <input 
                type="text" 
                required
                value={title}
                onChange={(e) => setTitle(e.target.value)}
            />
            <label>Blog body:</label>
            <textarea 
                required
                value={body}
                onChange={(e) => setBody(e.target.value)}
            />
            <label>Blog author:</label>
            <select
              value={author}
              onChange={(e) => setAuthor(e.target.value)}
            >
                <option value="mario">mario</option>
                <option value="yoshi">yoshi</option>
            </select>
            { isLoading? <button disabled>Adding Blog...</button> : <button>Add Blog</button> }
        </form>
    </div>
  );
}

export default Create;
```

#### 11.1.5. Deleting Blogs

We want the ability to delete a blog by clicking a button at the bottom of the BlogDetails component. We need to attach a click handler to the button tag and create a function, handleClick. We want to make a fetch request with takes in two arguments. We want a url to the /blogs/id endpoint. We have access to the blog id via id or blog.id, it does not matter which we decide to go with. The second argument is an object with simply a method of 'DELETE'. Fetch is an async call so we can chain the .then() method. Here we will redirect the user to the homepage (as it makes no sense for a user to stay on the page of a blog they deleted). We use the useNavigate hook again for this. Then add some CSS styling to make the button more aesthetic. Now we can delete any of the blogs, and return to the homepage afterwards!

BlogDetails.js:
```js
import React from 'react'
import { useNavigate, useParams } from 'react-router-dom'
import useFetch from './useFetch';

const BlogDetails = () => {
    const { id } = useParams();
    const { data: blog, error, isLoading} = useFetch('http://localhost:8000/blogs/' + id);
    const history = useNavigate();

    const handleClick = () => {
        fetch('http://localhost:8000/blogs/' + blog.id, {
            method: 'DELETE'
        }).then(() => {
            history('/')
        })
    }

  return (
    <div className="blog-details">
        { isLoading && <div>Loading...</div>}
        { error && <div> {error} </div>}
        { blog && (
            <article>
                <h2>{ blog.title }</h2>
                <p> Written by { blog.author }</p>
                <div>{ blog.body }</div>
                <button onClick={handleClick}>delete</button>
            </article>
        )}
    </div>
  )
}

export default BlogDetails
```

index.css:
```css
.blog-details button {
  background: #f1356d;
  color: #fff;
  border: 0;
  padding: 8px;
  border-radius: 8px;
  cursor: pointer;
}
```

NOTE: Moved the setTimeout() to useFetch as this is where the GET request is being made directly.

useFetch.js:
```js
import { useState, useEffect } from 'react';

const useFetch = (url) => {
   const [data, setData] = useState(null);
   const [isLoading, setIsLoading] = useState(true);
   const [error, setError] = useState(null);

   useEffect(() => {

    const abortController = new AbortController();

    setTimeout(() => {
    fetch(url, { signal: abortController.signal })
    .then(res => {
      if (!res.ok) {
        throw Error('Could not fetch the data for that resource')
      }
      return res.json()
    })
    .then((data) => {
      setError(null);
      setData(data)
      setIsLoading(false)
    })
    .catch(err => {
        if (err.name === 'AbortError') {
            console.log('fetch aborted');
        } else {
            setError(err.message);
            setIsLoading(false);
        }
    })
    }, 1000);

    return () => abortController.abort();
   }, [url]);

   return { data, isLoading, error }
}

export default useFetch;
```

#### 11.1.6. 404 Pages

This is for when we go to a URL that does not exist. We need to create a component for this called NotFound.js. We will make a simple template with a page cannot be found message, with a Link tag to the homepage. We need to add this component to the Route '*' in App.js. This path means that it catches any other route (not already specified). It goes at the bottom of the routes as it behaves as a catch all route. Do NOT place it first because it will match any route that comes in, it specifically goes at the bottom to not intercept the routes above it.

NotFound.js:
```js
import React from 'react'
import { Link } from 'react-router-dom'

const NotFound = () => {
  return (
    <div className="not-found">
        <h2>Sorry</h2>
        <p>That page cannot be found</p>
        <Link to="/">Back to the homepage...</Link>
    </div>
  )
}

export default NotFound
```

App.js
```js
import Navbar from './Navbar';
import Home from './Home';
import { BrowserRouter as Router, Route, Routes} from 'react-router-dom';
import Create from './Create';
import BlogDetails from './BlogDetails';
import NotFound from './NotFound';

const App = () => {
  return (
    <Router>
      <div className="App">
        <Navbar />
        <div className="content">
          <Routes>
            <Route path="/" element={<Home />} />
            <Route path='/create' element={<Create />} />
            <Route path='/blogs/:id' element={<BlogDetails />} />
            <Route path='*' element={<NotFound />} />
          </Routes>
        </div>
      </div>
    </Router>
  );
}

export default App;
```

## 12. Server-side Rendering
TBC

## 13. Testing
TBC
