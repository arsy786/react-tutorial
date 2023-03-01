# React Tutorial

All tutorials are from the Complete React Tutorial on the Net Ninja YouTube channel, [link is here](https://www.youtube.com/playlist?list=PL4cUxeGkcC9gZD-Tvwfod2gaISzfRiP9d).

## Lesson 1 - Creating a React App

### <ins>Steps for creating a React App:</ins>
1. Need node installed. Check version with `node -v`. If no version, install using brew with `brew install node`.
2. Run command `npx create-react-app app-name` in terminal to bootstrap a starter react project in current directory.
3. Change directory to the newly created react project and run command `code .` to open current directory (starter react project) in VSCode.
4. To run react app in dev mode run the command `npm start` and the application will run locally at at localhost:3000.

### <ins>What does the starter React Project contain?</ins>
There are a series of folders and files within the starter react project.

node_modules:

The folder node_modules contains all of the project dependencies, including the react library. Any packages or libraries installed in the future will always be stored in this location.

public:

The public folder contains all of the files that are public to the browser.

The index.html file within the public folder is the entry-point of the react app in the browser. 

All react code in injected into this 1 html file which is served to the browser. The exact location of this injection is in the div with id="root".

src:

The src folder contains 99% of the code you will write in react.

 App.js is a react component which contains child components. 

 There are also other CSS and JS files within this folder.

The index.js file is what kickstarts the application. It is responsible for taking all of the React components created and injected into App.js, and mounts them to the DOM.

### <ins>What can we remove from the starter React App?</ins>
The starter react project comes with some default files that render the starter page but these can be deleted immediately to help cleanup the project for the development of our own app.

Files to delete:

src:
- App.test.js, setupTests.js, logo.svg, reportWebVitals.js, index.css
public:
- All files except index.html

Code to edit/remove:

src: 
- logo.svg import in App.js,  
- reportWebVitals.js import in index.js
- index.css import in index.js
- clear the code inside of div in App.js (lines 6 to 19)
- convert App() function to arrow function in App.js
- keep App.css file but clear the clode.

public: 
- remove links to deleted files in index.html (line 5, 12 & 17) 
- remove comments in index.html
- change Title to something related to your project

Source: [How to create a React App & File Cleanup](https://www.youtube.com/watch?v=PAqbIbdvTuU)