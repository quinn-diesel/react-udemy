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
- once we get the information from the API we need to get the return response
- the question becomes about what do we use to grab the information
- the video detail and list will also be using
- DOWNWARDS DATA FLOW - only the parent should be able to get the information
- for now it's about using the most parent component that we are going to use to get the information. the APP is the parent
- the APP will be what is responsible for fetching the data

21 - Refactoring Functional Components to Class components
- we needs to set the state in the app
- the constructor will run when there is a change, which will run the YTSearch with the new list of videos
- notice that the data/videos function where the key and value are the same things
- there is a bit of es6 syntax that can be use used

23 - props
- we now have a search term that we can access the data that we need to get out to make what we need
- start with the video list
- there is the need for state
- we are using bootstrap with React so all the normal classes can be called
- here is the critical point to remember.
1. Make the component in the file.
2. Make sure to export the component so it can be used elsewhere.
3. Import to the main app.
4. Call the component where you need it in the div organisation.
- need to pass parent information to the child component -> define the property in the JSX tag
- passing information from App to the render is a PROP.
- anytime the app re-render the videolist will get the new list that we are using
- sometimes when the request is still completing we might see a 0 with what is going on
- class based component props is available anywhere with this.props
- whenever refactor to a function component to a class component props needs to be changed from props to this.props

24 - Building Lists with Map
- try to use in built in iterators that are going to be used
- an idea might be to use Map
- the idea is to array.map that will automatically iterate over it
- array.map(function (number) { return number * 2}) will return an array that is twice what is happening
- you can add divs with JSX and get a list that we want
- react is really intelligent about arranging an array of elements that React that will be a list that can be done inside of the UL

25 - List Item Keys
- React can be a bit too smart when rendering an array of items and building a list
- there is a lot of programming that is being used to have it's information updated
- if you have an id then you can update the correct part of the deck of cards
- React builds a list when it has an ID so it knows where to go and update
- think about where the element is in the deck of cards
- the response has an e-tag that is a long string of characters that is a key that be used in the videoitems array


26 - Video List Items
- {video} this is the same as const video = (props) =>
- create a new variable with ES6 syntax
- {referencing variable}

27 - Detail component
- Question to ask for new component: Does the component need to maintain any kind of state?
- video details needs to have
- we can craft our own video URL id
-   const url = 'https://www.youtube.com/embed' + videoId;
- this is creating the youtube video player in the application we are using
- ${videoId}'  = +  videoId; helps when making the string with interpolation
- iframe you just have to provide a source and place whatever content you need

28 - Handling Null props
- the app will always try to automatically render the search that we are looking for
- in the videodetail we make a check to see if there is no video. that way there won't be a rendering problem on the first load
- if(!video) = if there is no video then return(exit) and render nothing
- this needs to be the first thing on the list that I am doing

29 - Video Selection
- want to have an ajax spinner on a high level component
- we want to give the user the ability to click on a video and see what is going on
- we will have a callback that will be in app that will be called when the videolist is clicked
- first pass the video into the videoDetail
- created the selectedVideo to start at Null
- at the same time as the loading the ajax request is sent to get the video
- we select the first video to playe
- then there is a re-render with AJAX and we get the first video
- onVideoSelect = {selectedVideo => this.setState({selectedVideo})} function which defines the selectedVideo in the app state
- passing a function which manipulates another function
- we are now taking the function to go BACK into the video list
- this is going back through the list of components together so each items can work together
- this is calling parent downwards to the child. passing callbacks like this is ok to pass information back and forth

30 - Styling with CSS
- there is still plenty of work to do, but this is just normal CSS
- :hover is a pseudo code that can be used for the hover of something

31 - adding in the search bar
- it's all about tracing how the events are going to work

32 - Throttling the search terms
- we want to try and kick off what people are searching in better way
- we want to make use of a functional library called lodash
- throttle useing debouce (this is in the 30 days of js coding)
- debounce creates a new function that will only be called once every 300 ms
- this is a great way to throttle what people are using

33 - React WrapUp
- this is the first React application
- Concept 1: class based vs functional: class is used whenever there is state in the component. functional is used when there is the same functional
- Concept 2: set the state inside of the constructor
- whenever we change the state everything re-renders
- Import and export statements - this is when we require files in and what we want to use
- Wherever we use the library we just get the name of the library
- How often we use callbacks - we only used a few
- Redux themed applications there are less callbacks in the confusing fashion
- Callbacks exist in order to parent-children communication
- whenever we change searchbar state it only changes the state for that specific component
- when we are talking about state it is very component level. there is always application level.


----- SECTION 3 - MODELING APPLICATION STATE ------

34 - Intro
- Redux is a very broad topic across lots of things
- The idea is how to model Redux with what is going on. Build something on what we are doing
- The goal is to make everything as clear as possible

35 - What is the main difference?
- Redux is a predictable state framework
- There are two parts to displaying books
- Back-end data you have a list of books and the currently selected books
- The views are all the items that we have made
- You use the data and the views and merge them together to make an applications

36 - Redux is the data contained in the Back-end
- state container - collection of all the data that describes the books
- react really shows the views that the user will interact with
- it is about centralising the data into a single object.
- usually there are collections of information
- the centre object is the Redux state - the data of the applications
- First example of FLUX - counter:
- Data: current counter the views are the current count and the number change
- Redux will just keep track of the current counter. This is the state of the application.

37 - Even more Redux EXAMPLE
- Having the best sense of state one of the most important things happening
- Tinder is a great example
- We need to have a list of information
- Everything will sit in one single object that is the application state

----- SECTION 4 - PUTTING REDUX TO PRACTICE ------

39 - Reducer
- what is a reducer?
- function that returns a piece of the application state
- becuase there can be many different forms of state there can be many different statements
- one state for the full list of books
- one state for active books that have been
- there is a reducer produce the value of the state
- the only thing the reducer is worth is the value and key of the state
- we should just get an array of objects

40 - ReactRedux
- this is used to link react and redux together so the information can be pulled from the redux back-end to the react front-end
- we are going to create a container
- container is a react component that is connected to the state managed by redux
- this is the BRIDGE that will link the redux back-end and the react front-end

41 - Containers Continued
- a container is a component that has direct access to the states that are created in redux
- that is the only way to get access to a component that is in Redux
- we want the most parent component to care about the state and the list of books
- Smart components or Containers are what have access
- the easy way, just make app as a container and render
- only create containers that care about state
- this is about fragmenting the containers in the app so it only pertains to what you need it to
- bookslist needs to connect to the book list

42 - Combining
- book list and book detail are the only components that need to have a 
- app should just be a component that doesn't have any touch of any data that is handled in the back-end
- we only create containers that care about a piece of state and what it's doing
- Import from react-redux this is the import connect react-redux
- connect takes a function and a component and produces a container
- a container is aware of the state that is done in redux
- the first object is a state that is an object that is available that is available to the this.props in the container
- if our state every changes our list will re-render out new list of books
- whenever our appiclation state changes

43 - 
- our application state is generated by the reducer states
- the books reducer always returns an array of objects, which has an