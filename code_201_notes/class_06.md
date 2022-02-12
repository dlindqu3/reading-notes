# Code 201 Reading Notes 
### 6. Read: 06 - JS Object Literals, the DOM

#### JS notes 
####  source: Jon Duckett: "JAVASCRIPT & JQUERY", 2014 [link](https://www.amazon.com/JavaScript-JQuery-Interactive-Front-End-Development/dp/1118531647/ref=sr_1_3?crid=181UMRLMS9TYB&keywords=duckett+javascript+jquery&qid=1643908836&sprefix=ducket+javascript+jquerry%2Caps%2C55&sr=8-3)

```
Chapters:   
Chapter 3 (100-105): object literals
Chapter 5 (183-242): "document object model" 
```

**Chapter 3: object literals**  
```javascript
let myObj = {
  name: 'salah',
  position: 'forward', 
  goalsEpl: 16,
  goalsCl: 7
  active: true,
  function getTotalGoals (goalsEpl, goalsCl){
    return this.goalsEpl + this.goalsCl
  }
}
myObj.name; 
myObj['name']; 
myObj.getTotalGoals(); 
```

**Chapter 5: document object model**
```javascript 
document.getElementById("name"); 
document.getElementsByClassName("greeting")[0]; 
document.getElementsByTagName("h1"); 
querySelector("h1.greeting"); //uses CSS selectors
querySelectorAll("#name, #address"); //uses CSS selectors 
```
- siblings, children 
- elements/nodes; elements are more specific 
- nodes include non-html elements
- selectors return a NodeList or a HTMLCollection 
- adding content with innerHTML can lead to security issues