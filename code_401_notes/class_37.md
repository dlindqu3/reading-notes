# Code 401 Reading Notes 
### 37. React 1

####  source: Tania Rascia, "ES6 Syntax and Feature Overview" [link](https://www.taniarascia.com/es6-syntax-and-feature-overview/)
- var, let, const

```javascript 
function func(a, b, c) {} // function declaration
var func = function (a, b, c) {} // function expression

let func = (a) => {} // parentheses optional with one parameter
let func = (a, b, c) => {} // parentheses required with multiple parameters

for (let i of arr) {
  console.log(i)
}

let func = (a, b = 2) => {
  return a + b
}

func(10) // returns 12
func(10, 5) // returns 15


let arr1 = [1, 2, 3]
let arr2 = ['a', 'b', 'c']
let arr3 = [...arr1, ...arr2]

console.log(arr3) // [1, 2, 3, "a", "b", "c"]


class Inheritance extends Func {
  constructor(a, b, c) {
    super(a, b)

    this.c = c
  }

  getProduct() {
    return this.a * this.b * this.c
  }
}

let y = new Inheritance(3, 4, 5)
```

####  source: "State and Lifecycle" [link](https://reactjs.org/docs/state-and-lifecycle.html)

```javascript 

class Clock extends React.Component {
  constructor(props) {
    super(props);
    this.state = {date: new Date()};
  }

  componentDidMount() {
    this.timerID = setInterval(
      () => this.tick(),
      1000
    );
  }

  componentWillUnmount() {
    clearInterval(this.timerID);
  }

  tick() {
    this.setState({
      date: new Date()
    });
  }

  render() {
    return (
      <div>
        <h1>Hello, world!</h1>
        <h2>It is {this.state.date.toLocaleTimeString()}.</h2>
      </div>
    );
  }
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Clock />);

```

#### source: "Handling Events" [link](https://reactjs.org/docs/handling-events.html)

```javascript 
class Toggle extends React.Component {
  constructor(props) {
    super(props);
    this.state = {isToggleOn: true};

    // This binding is necessary to make `this` work in the callback
    this.handleClick = this.handleClick.bind(this);
  }

  handleClick() {
    this.setState(prevState => ({
      isToggleOn: !prevState.isToggleOn
    }));
  }

  render() {
    return (
      <button onClick={this.handleClick}>
        {this.state.isToggleOn ? 'ON' : 'OFF'}
      </button>
    );
  }
}


<button onClick={(e) => this.deleteRow(id, e)}>Delete Row</button>
<button onClick={this.deleteRow.bind(this, id)}>Delete Row</button>
```

#### source: "Utility-First Fundamentals" [link](https://tailwindcss.com/docs/utility-first)
- With Tailwind, you style elements by applying pre-existing classes directly in your HTML

```html
<div class="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-lg flex items-center space-x-4">
  <div class="shrink-0">
    <img class="h-12 w-12" src="/img/logo.svg" alt="ChitChat Logo">
  </div>
  <div>
    <div class="text-xl font-medium text-black">ChitChat</div>
    <p class="text-slate-500">You have a new message!</p>
  </div>
</div>
```

#### source: "Create a Next.js App" [link](https://nextjs.org/learn/basics/create-nextjs-app)
- page-based routing, with dynamic routes
- API routes for serverless functions
- steps: 
  - npx create-next-app nextjs-blog --use-npm 
  - cd nextjs-blog
  - npm run dev

#### source: "Why I’m Using Next.js in 2020" [link](https://www.youtube.com/watch?v=rtgbaKBhdkk)
- can render on client or server or both
- can handle static and dynamic pages well 
- real time rendering should be from server 

#### Things I want to know more about 
-  next.js