# Code 301 Reading Notes 
### 3. Read: 03 - Passing Functions as Props 

####  React Docs - lists and keys 
####  source: "Lists and Keys",  [link](https://reactjs.org/docs/lists-and-keys.html)

**Lists and Keys**  
- 1. .map() returns a new array 
- 2. use a method like .map() and render each new <li> inside a pre-made <ul>, as seen below 
- 3. each list item needs a unique key 
- 4.  keys tell React which elements have been changed, and give each element a set identity 

```javascript 
function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    <li key={number.toString()}>
      {number}
    </li>
  );
  return (
    <ul>{listItems}</ul>
  );
}

const numbers = [1, 2, 3, 4, 5];
ReactDOM.render(
  <NumberList numbers={numbers} />,
  document.getElementById('root')
);

```

####  The Spread Operator 
####  source:  "How to Use the Spread Operator (...) in JavaScript",  [link](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

**The Spread Operator**
- 1. this iterates through a javascript arrays or object literals  and passes each value in it through the given function 
- 2. it can be used to include elements in a list; in can work with objects of varying length; it can be used to add a new value to a given data store; it can be used to pass arguments into a function 
- 3. see below 

```javascript 
let nums = [1,2,3]; 
let letters = [a,b,c]; 
let numLetters = [...nums, ...letters]; 
```

- 4. see below 

```javascript 
let nums = [1,2,3]; 
let newNum = [5]; 
let allNums = [...nums, newNum]; 
```

- 5.  see below 

```javascript 

let person = {
  name: 'bill', 
  age: 70
}

let job = {
  position: 'science guy', 
  specialty: 'education'
}

let scientist = {
  ...person,
  ...job
}


```

####  How to Pass Functions Between Components
####  source:  "React - How to Pass Functions between Components - Episode 22",  [link](https://www.youtube.com/watch?v=c05OL7XbwXU)


**How to Pass Functions Between Components**
- 1. first step to pass a function between components: create the relevant function
- 2. what does the increment function do: add one to this.props.count
- 3. to pass an element from a parent to child component: use props
- 4. the child component invokes a method passed from a parent by: passing the method in the child component like a prop 



## Things I want to know more about 
-  how to pass functions between components; how to invoke a method in a passed function 