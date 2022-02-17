# Code 201 Reading Notes 
### 9. Read: 09 - Forms and Events 

####  HTML notes 
####  source: Jon Duckett: "HTML & CSS", 2011 [link](https://www.amazon.com/HTML-CSS-Design-Build-Websites/dp/1118008189/ref=pd_bxgy_img_1/136-1383517-8048428?pd_rd_w=oqCBX&pf_rd_p=6b3eefea-7b16-43e9-bc45-2e332cbf99da&pf_rd_r=ZS5VB2D5THCC2NQKK0H1&pd_rd_r=d97ebdc9-d149-47e2-9f7d-2126282e1221&pd_rd_wg=rvnoS&pd_rd_i=1118008189&psc=1)

```
Chapters:     
Chapter 7 (144-175): forms
Chapter 14 (330-357): lists, tables, and forms 
```

**Chapter 7: forms**  
- ```<form></form>```
- ```<input></input>```
- ```<textarea></textarea>```
- ```<select></select>```
- ```<option></option>```
- ```<label></label>```


**Chapter 14: lists, tables, and forms**  
-  ```<ul></ul>```
- ```<ol></ol>```
- ```<li></li>```
- ```<table></table>```
- ```<form></form>```


#### JS notes 
####  source: Jon Duckett: "JAVASCRIPT & JQUERY", 2014 [link](https://www.amazon.com/JavaScript-JQuery-Interactive-Front-End-Development/dp/1118531647/ref=sr_1_3?crid=181UMRLMS9TYB&keywords=duckett+javascript+jquery&qid=1643908836&sprefix=ducket+javascript+jquerry%2Caps%2C55&sr=8-3)

```
Chapters:   
Chapter 6 (243-292): events
```

**Chapter 6: events**  
- element.onEvent = functionName;
- element.addEventListener('event', functionName, capture(usually set to false)); 
- event object "e" 

```javascript 
let el; 
el.addEventListener('click', myFunc, false); 

```