# Code 201 Reading Notes 
### 7. Read: 07 - HTML Tables, JS Constructor Functions 

####  HTML notes 
####  source: Jon Duckett: "HTML & CSS", 2011 [link](https://www.amazon.com/HTML-CSS-Design-Build-Websites/dp/1118008189/ref=pd_bxgy_img_1/136-1383517-8048428?pd_rd_w=oqCBX&pf_rd_p=6b3eefea-7b16-43e9-bc45-2e332cbf99da&pf_rd_r=ZS5VB2D5THCC2NQKK0H1&pd_rd_r=d97ebdc9-d149-47e2-9f7d-2126282e1221&pd_rd_wg=rvnoS&pd_rd_i=1118008189&psc=1)

```
Chapters:     
Chapter 6 (126-145): tables
```

**Chapter 6: tables**  
- ```<table></table>```
- ```<th></th>```
- ```<tr></tr>```
- ```<td></td>```


#### JS notes 
####  source: Jon Duckett: "JAVASCRIPT & JQUERY", 2014 [link](https://www.amazon.com/JavaScript-JQuery-Interactive-Front-End-Development/dp/1118531647/ref=sr_1_3?crid=181UMRLMS9TYB&keywords=duckett+javascript+jquery&qid=1643908836&sprefix=ducket+javascript+jquerry%2Caps%2C55&sr=8-3)

```
Chapters:   
Chapter 3 (106-144): functions, methods, and objects  
```

**Chapter 3: functions, methods, and objects**  
```javascript
//constructor 
function Dog (name, breed, age){
  this.name = name;
  this.breed = breed; 
  this.age = age
}
let dog1 = new Dog('Chewy', 'lab', 5); 
```