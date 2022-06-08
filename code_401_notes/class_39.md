# Code 401 Reading Notes 
### 39. React 3

####  source: "Learn useContext In 13 Minutes" [link](https://www.youtube.com/watch?v=5LrDIWkK_Bc)
- pass a value in ThemeContext.Provider 
- import hook useContext


####  source: Reed Barger, "React Context for Beginners – The Complete Guide (2021)" [link](https://www.freecodecamp.org/news/react-context-for-beginners/#what-is-react-context)
- react context is a way of sharing data across app without using props 
- data should be shared via context if it does not need to be updated often 
- the context is the equivalent of global variables for our react components
- steps to use: 
  - create context 
  - wrap context provider around component tree
  - add values to context
  - read values as needed within components 

####  source: "Create a Next.js App" [link](https://nextjs.org/learn/basics/create-nextjs-app)
- to create new pages in Next.js app, create a .js file under "pages" directory 
- wrap links in <Link></Link> tags 
- next.js does code splitting automatically, so it only loads data needed for given page 
- put static files in "public" directory 



#### Things I want to know more about 
- I still don't really understand the useContext hook 