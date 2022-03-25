# Code 301 Reading Notes 
### 10. Read: 10 -  In Memory Storage 

####  source: Charles Freeborn, "The JavaScript Call Stack - What It Is and Why It's Necessary" [link](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4)

1. a call is the invocation of a function. 
2. one call can happen at once.  
3. LIFO - last in first out. 
4. see below

![this is an image](./static/call%20stack.png)

```javascript 
function getConcatString(str1, str2){
  let str3 = str1 + str2;
  return str3;  
}

function getConcatStringLength(){
  let str = getConcatString('hello', 'goodbye')
  return str.length; 
}

```
5. A stack overflow is caused by a recursive function that does not have an exit point. 


#### source: Diogo Spinola, "JavaScript error messages && debugging" [link](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c) 

1. a reference error is an error that occurs if a necessary variable has not been declared.
2. a syntax error is an error related to faulty syntax, like doing .length on a function. 
3. a range error is an error that involves trying to find part of an array, object, etc. that is outside of current scope. For instance, if the array has length 5, and you try to get array[7], you will see this error. 
4. a type error is an error that involves incompatible types, like trying to find .length of an undefined variable. 
5. a breakpoint is a developer-set stopping point in the call stack used to spot errors. 
6. if placed in the code, the word "debugger" will trigger a breakpoint. 

## Things I want to learn more about: 
- recursive functions and common applications 