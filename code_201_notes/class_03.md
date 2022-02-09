# Code 201 Reading Notes 
### 3. Read: 03 - HTML Lists, Control Flow with JS, and the CSS Box Model

####  HTML notes 
####  source: Jon Duckett: "HTML & CSS", 2011 [link](https://www.amazon.com/HTML-CSS-Design-Build-Websites/dp/1118008189/ref=pd_bxgy_img_1/136-1383517-8048428?pd_rd_w=oqCBX&pf_rd_p=6b3eefea-7b16-43e9-bc45-2e332cbf99da&pf_rd_r=ZS5VB2D5THCC2NQKK0H1&pd_rd_r=d97ebdc9-d149-47e2-9f7d-2126282e1221&pd_rd_wg=rvnoS&pd_rd_i=1118008189&psc=1)

```
Chapters:     
Chapter 3 (62-73): lists
Chapter 13 (300-329): boxes
```

**Chapter 3: lists**  
- ```<ol></ol>```
- ```<ul></ul>```
- ```<li></li>```

**Chapter 13: boxes**
- div {height: 50%; width: 50%; background-color: yellow;}
- min-width, max-width
- min-height, max-height
- p {overflow: scroll;}
- border, margin, padding 
- border-width, border-style, border-color 
- center content: set left and right margins to "auto" 


#### JS notes 
####  source: Jon Duckett: "JAVASCRIPT & JQUERY", 2014 [link](https://www.amazon.com/JavaScript-JQuery-Interactive-Front-End-Development/dp/1118531647/ref=sr_1_3?crid=181UMRLMS9TYB&keywords=duckett+javascript+jquery&qid=1643908836&sprefix=ducket+javascript+jquerry%2Caps%2C55&sr=8-3)

```
Chapters:   
Chapter 4 (162-182): decisions and loops 
```

**Chapter 4: decisions and loops**  
```javascript
switch(num){
  case 7: 
    console.log('the num matches one of the targets, 7'); 
    break; 
  case 5: 
    console.log('the num matches one of the targets, 5');
    break; 
  default: 
    console.log('the num does not match any of the targets'); 
} 
```
- avoid problems with type coercion by using ===
- falsy values: ```false```, 0, '', 10/'string',  undefined (a variable with nothing assigned to it), null, NaN
-truthy values: everything else 
- short-circuit values: an expression with logical operators is evaluated from left to right. if the given condition is met and the rest of the expression won't effect the current result, the expression will return the given result
- short-circuit example: 

```javascript
let a; 
let b = 5; 
let c = 6; 
let num = a || b || c; 

//here, num will be assigned to 5. 
```
- loops:  
- keywords: break, continue 

```javascript 
let arr = [1,2,3,4,5]; 
for (let i = 0; i < arr.length; i++){
  if (arr[i] === 4){
    break; 
  }
  console.log(arr[i]); 
}
for (let i = 0; i < arr.length; i++){
  if (arr[i] === 4){
    continue; 
  }
  console.log(arr[i]); 
}
```
```javascript 
let a = 5; 
while (a > 0){
  console.log('hello'); 
  a--; 
}
```



