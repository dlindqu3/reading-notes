# Code 301 Reading Notes 
### 2. Read: 02 - State and Props 

####  React Lifecycle 
####  source: Joshua Blankenship: "React: Component Lifecycle Events",  [link](https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093)



**React: Component Lifecycle Events**  
- 1. render occurs first, before componentDidMount
- 2. mounting is the first thing to happen in the React lifecycle
- 3. correct order: constructor, render, componentDidMount, React Updates, componentWillUnmount
- 4. the componentDidMount is used here to connect to the Youtube API 

**React State vs Props**
- 1. counters, titles/subtitles
- 2. difference: props are handled outside of a component and passed into a component, while state  is handled inside of a component and you can update it inside a component
- 3. we re-render our application when we change the state 
- 4. things we could store in state: things that will update/re-render 
