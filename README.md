# React Tutorial

All tutorials are from the Complete React Tutorial on the Net Ninja YouTube channel, [link is here](https://www.youtube.com/playlist?list=PL4cUxeGkcC9gZD-Tvwfod2gaISzfRiP9d).

## Lesson 1 - Creating a React App

1. Need node installed. Check version with `node -v`. If no version, install using brew `brew install node`.
2. Run command `npx create-react-app app-name` in terminal to bootstrap a starter react project.
3. Change directory to new react project and run command `code .` to open current directory (starter react project) in VSCode.
4. To run react app in dev mode run the command `npm start` and the application will run locally at at localhost:3000.

There are a series of folders and files within the react project.

node_modules:
- The folder node_modules contains all of the project dependencies, including the react library. Any future packages or libraries installed in the future will be stored in this location.

public:
- The public folder contains all of the public files that are public to the browser.
- The index.html file within the public folder is the entry-point of the react app in the browser. All react code in injected into this 1 html file which is served to the browser. The exact location of this injection is in the div with class "root".

src:
- The src folder contains 99% of the code you write in react. App.js is a react component. There are also other CSS and JS files within this folder.
- The index.js file is what kickstarts the application. It is responsible for taking all of the React components created, and mounting them to DOM.


The starter react project comes with some default files that render the starter page but these can be deleted immediately.

Delete:
- in src folder Delete: App.test.js, logo.svg (and its import in App.js), reportWebVitals.js (and its import and code in index.js), setupTests.js, index.css (and its import in index.js), code in App.js (lines 6 to 19), convert App() function to arrow function in App.js, keep App.css but clear clode.
- in public folder Delete: Remove all files except index.html, remove line 5, 12 & 17 (links to deleted files) in index.html, remove comments in index.html, change Title

Source: [How to create a React App & File Cleanup](https://www.youtube.com/watch?v=PAqbIbdvTuU)