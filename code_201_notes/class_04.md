# Code 201 Reading Notes 
### 4. Read: 04 - HTML Links, CSS Layout, JS Functions
####  HTML notes 
####  source: Jon Duckett: "HTML & CSS", 2011 [link](https://www.amazon.com/HTML-CSS-Design-Build-Websites/dp/1118008189/ref=pd_bxgy_img_1/136-1383517-8048428?pd_rd_w=oqCBX&pf_rd_p=6b3eefea-7b16-43e9-bc45-2e332cbf99da&pf_rd_r=ZS5VB2D5THCC2NQKK0H1&pd_rd_r=d97ebdc9-d149-47e2-9f7d-2126282e1221&pd_rd_wg=rvnoS&pd_rd_i=1118008189&psc=1)

```
Chapters:     
Chapter 4 (74-93): links
Chapter 15 (358-404): layout
```

**Chapter 4: links**  
- ```<a href="google.com">Google</a>```
- ```<a href="index.html">Home</a>```
- ```<a href="mailto:johndoe@gmail.com">email john</a>```

**Chapter 15: layout**  
- block-level elements vs inline elements 
- floating elements 
- you can create multi-column layouts using floats 
- layout grids can allow a page to adjust to different screen sizes 


#### JS notes 
####  source: Jon Duckett: "JAVASCRIPT & JQUERY", 2014 [link](https://www.amazon.com/JavaScript-JQuery-Interactive-Front-End-Development/dp/1118531647/ref=sr_1_3?crid=181UMRLMS9TYB&keywords=duckett+javascript+jquery&qid=1643908836&sprefix=ducket+javascript+jquerry%2Caps%2C55&sr=8-3)

```
Chapters:   
Chapter 3 (86-99): functions, methods, and objects
```

**Chapter 3: functions, methods, and objects**  
- parameter: values that specified for use in a function at time of declaration
- argument: values passed into the function when it's called 

```javascript 
//named function 
function areaSquare(length, width){
  return length * height; 
}

//anonymous function 
let areaTriangle = function (base, height){
  return 0.5 * base * height; 
}

//immediately invoked function expressions (IIFEs)
let areaCircle = (function (){
  let radius = 5; 
  return (radius ** 2) * 3.14; 
}()); 

//Scope 
let a = 5 //global scope 

function myFunc(){
  console.log(a); 
  let a = 10; //local scope 
  console.log(a); 
}

//block scope: within {} of a if, for, or while statement
//lexical scope: children scope can access elements defined in the parent scope

```
- IIFEs are often used in event handlers to make something happen when an event happens
- IIFEs are often used as a wrapper around a chunk of code to isolate it from other parts of the program 

#### source: "6 Reasons for Pair Programming", by Allie Grampa, 2018 [link](https://www.codefellows.org/blog/6-reasons-for-pair-programming/)

**6 Reasons for Pair Programming**
- improve efficiency
- improve collaboration 
- learn from classmates
- improve social skills
- prepare for interviews
- prepare for work 
