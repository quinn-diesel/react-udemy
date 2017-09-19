Here are the notes that I will write down from the course. These can be used as a point of reference later.

It will also help me to write better readmes in the future hopefully.

----- SECTION 1 - INTRODUCTION TO REACT ------

3 - web pack and web pack are going to be the transpilers that are going to be used by the browser
4 - node program manager install and then npm start to get it all started

5 - remember components are what are mashed together to make different things
- it is these components that will be ultimately used in html

6 - you have to tell the html to generate the component
const: this is declaring a variable, the only difference, this will be the final variable. it will be constant! you won't re-assign what this is going to be later.
jsx: subset of js that looks like html that is actually js. webpack and babel are going to the code transpilling.

7 - we use const because this will never change at any time
- JSX cannot be interpreted by the browser, this is what webpack and babel are going to be used for
- why JSX? this is what produces the actual HTML that gets inserted into the DOM when we render (place the components onto the page).
- HTML into page into what we want to see
- JSX - produce html so the person can use this
- don't have to write JSX get transpiled to vanilla javascript
- get compiled but it's really ugly.
- JSX is more readabl overall

8 -  when we write Es6 we have access to javascript code. all the code that is written is silo'd.
 code that is declared in other models unless it is explicity said.
 you can't make reference to any variables that are in that file
 you have to explicity say what you want to have access to.

9 - React knows how to
- to take a component and render it to the DOM you have to use a separate library called reactDOM

10 - we could have many different instances of app. this is a class not an instance
- app is the 'factory' of the things that are going to be rendered to the DOM
- instantiate components before rendering to the DOM
- when you write DIV in JSX it will write it as a class and turn it into an instance for us
- < /> now passes from a class to a instance

11 - whenever we have to make a component, we have to wrap it in JSX tags
- the react DOM takes a seconda argument
- this is a target DOM element
- App, and then insert into the HTML document
- most react apps you are going to load the div with something with class container
- root node of the entire react active
- everything will be nested into the root element
- new es syntax
- => fat era

12 - component is a function or object that returns some sort of html
  - might have a single component that does each aspect of the
  - react knows how to render a lot of components all at once really fast
  - the idea is to spread out different component across the app
  - it's a somewhat arbitrary way of doing the components
  - this will be for me to decide
  - EXAMPLE: a search bar will be one compononent all by itself
  - one for the vidoe and the title and description
  - another one that represents the rest
  - nesting is to have one compononent that will have multiple components in it
  - there will be a lot going on but it's about folding it all up into itself

13 - 
