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

13 - youtube api
- two step process: we need to get the youtube key and password
- API key to identify ourselves
- install a small package to help make the seaching process easy
- the package json file is the list of all the packages that are going to use what we need

14 - export statements
- exporting models, classes and state:
- we need to make sure the user can see the div
- react components can see other components. we need to get it into index.js
- remember all the files are silo'd from each other
- we only want to export a subset of code we want to work from
- it is very important to export each of the files that we have
- we have to give a file reference when we are importing
- created the component, exported it from the file, then imported it to the index and then rendered the search bar in the App file

15 - creating a component with an es6 flash
- a class component is used for internal record keeping
- Because users are going to be typing into the input we want to register what people are typing
- right now it's a functional component
- class component - object with a set of criteria
- functional component to a class based component


16 - handling user errors
- first declare event handler - run whenever the event occurs
- pass the event to the monitor
- onInputChange or handleChange, you should be able to tell the purpose of the method
- all events that get triggered, they are called with the event handler (event)
- this describes the context that is happeneing, can use the event object to get access to the event output
- input with an event handler, specifically we are calling the onChange property
- in the class we define another element

17 - introduction to state
- state: plain javascript object that is used to record and respond to user-based events
- each class has it's own state object
- each time the state is changed it forces the render to change, and the render function is re-run. it will apply to all the children
- you have to intiliase the state object
- set the state to a plain object
- all js functions have a constructor, this is called automatically anytime the instance is created, the function is called anytime there is a new instance of the SearchBar
- the constructor function is used to set up state and other variables
- component itself has it's own parent method
- super will call the parent class with the idea of super
- the object you pass to the this.state will be what you want see in the search term
- as the user starts typing in the input, we want it to be the value of the input

18 - state continued
- state is a plain js object that exists on any component that is a class based component. each one will have it's own copy of state
- you will set the state with this.state. you can use any property name for the term
- updating the state is different from updating the state
- constructor function (this.state) will be the only time you see it.
- it will usually this.setState({ object you want to manipulate })
- use the method to inform react about what is going on
- whenever we change our state, it updates out updated method in the DOM
- this is the full circle of the state
- whenever you want to update a component you want to use state

19 - controlled components
- only update state with this.setState
- the only time it is done manually is in the constructor
- control field is the form element that is set by the state
- whenever our input change it tells the input what the state should be
- a controlled component is change by the state. this is only changed when the state is changed
- when the setState makes a re-render this changes the above value.
- the idea is the first value is nothing, then when the user types something it triggers the setState which changes the value of the input
- this is how data is changed, there is no imperative form of data.
- KEY: THE VALUE OF THE INPUT IS EQUAL TO THE STATE
- it allows to preset elements.

20 - breather and review
- remember app is a functional component because it doesn't have a state based component

----- SECTION 2 - AJAX REQUESTS WITH REACT ------

21 - Youtube Search Response
