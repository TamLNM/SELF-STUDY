# THIS PROJECT IS FOR MY SELF-STUDY

## I. DATA - DATA TRANSFER
### 1. JSON:

<img src="https://github.com/TamLNM/SELF-STUDY/blob/master/images/json-logo.png" width="200">

- Stands for "JavaScript Object Notation"
- Is data representation Format
- Commonly Used 4 APIs and Configs
- Can read and understand by multiple programming language - Lightweight - Easy to intergate
- Is opened-standard for data transfer in the internet
- Data: String, Number (any form), Booleans, null, Array, Object
- Uses: key/value, name/value
- <b>JSON OBJECT</b>: "json_variable" : <object>
Example: { "firstName": "Le Nguyen Minh", "lastName" : "Tam" }
- <b>JSON Arrays</b>: "json_variable" : <object>
Example: [ { "firstName": "Le Nguyen Minh", "lastName" : "Tam" } , { "firstName": "Nguyen Van", "lastName": "A" }
- <b>Function covert a json string into javascript object</b>
`var obj = JSON.parse(text);`
  

## II. CODE - USEFUL EXTENSIONS
### 1. <b>Emmet</b> - Extension for coding speed inscreasing

- Extension name: <b>EMMET</b>, I usually use Mithril Emmet
- A new HTML base code: <i>html:5</i>, <i>html:xt</i>.
- A element with classes: <i>element.class1.class2.(...)</i> + tab
<br><b><i>Ex:</i></b> div>div.class + tab
- A element with id: <i>element#id</i>
<br><b><i>Ex:</i></b> div# + tab
- A parent tree include multiple tab: <i>parent>child>child_of_child>...</i> + tab
<br><b><i>Ex:</i></b> div>p.class1>a + tab
- Create elements in the same lever: <i>element_1 + element_2 + element_3</i> + tab
<br><b><i>Ex:</i></b> header+article+footer + tab
- Create a example text: <i>lorem<number of character you want to create></i>
<br><b><i>Ex:</i></b> lorem20 + tab
<br>--> Lorem ipsum dolor sit, amet consectetur adipisicing elit. Et repellendus quam voluptatibus possimus molestias ullam accusamus deserunt in voluptas amet.
- Create multiple elements: <i>element*number_need_create</i>

## III. JAVASCRIPT
### 1. About the ECMAScript Editions:
- We have about six version of ECMA Script, include ES1 - ES6, with 2 nearest function:
+ ES5: edition in 2009
+ ES6: edition in 2015 - 2018
- Browers support for ES5: Chome ver23, IE ver9*/10, Edge ver10,...
<i>* Internet Explorer 9 does not support ECMAScript 5 "use strict".</i>
<i>Internet Explorer does not support ECMAScript 2015.</i>

### 2. ES5 Features
Includes:
- use strict
- String.trim()
- Array.isArray()
- Array.forEach()
- Array.map()
- Array.filter()
- Array.reduce()
- Array.reduceRight()
- Array.every()
- Array.some()
- Array.indexOf()
- Array.lastIndexOf()
- JSON.parse()
- JSON.stringify()
- Date.now()
- Property Getters and Setters
- New Object Property Methods
#### a. Use strict
You can understand it as a "stict" mode, more difficult, more rules than tthe standard mode.
Use for:
- Prevent use, throw errors with the unsafe processing.
- Disable confuse features or shouldn't use.
- Prevent some work can be a key word in the future
Command: 
`use strict`
The place you put the command `use strict` specified the affected area of strict mode.
Examples:
1. 
```
"use strict";
function foo(){
    var bar = 0;
    return bar;
}

// Uncaught ReferenceError: bar is not defined
bar = 1;
```



## ABBREVIATIONS + TERMINOLOGY
1. EMCA (in EMCAScript): stands for "European Computer Manufacturer's Association". Can understand like ECMAScript is the modal in build on paper and javascript is the programming language to make it in computer to feel more easily.

## DOCUMENTATION
1. [(Vie) How to use Markdow - Write text for Github](https://viblo.asia/helps/cach-su-dung-markdown-bxjvZYnwkJZ)
2. [(Vie) Codehub Emmet](https://www.codehub.com.vn/Viet-HTML-Nhanh-Hon-Voi-Emmet)
3. [(Eng) W3Schools](https://www.w3schools.com/)
 
## MY SELF-STUDY NOTES:
1. [(Eng) How to covert HTML, CSS, Javascript into Wordpress - Step to do](https://docs.google.com/document/d/1xp-I7kgeLrttyS3ySjwmyGjvt7wh09t4Hn91B2fujmY/edit?usp=sharing)
2. [(Eng) LARAVEL - Note for my Laravel approach](https://docs.google.com/document/d/14ZGjTyPZ7bHScMhA-o58TIGme7s2kmvbapcK34KDFn4/edit?usp=sharing)
3. [(Eng) LARAVEL - APIs](https://docs.google.com/document/d/1Qh4YJ4vAGv_aqwHtzTQNNI--2wbvrNXHzntoJ8z4Hj8/edit?usp=sharing)
4. [(Eng) LARAVEL - My first documentation for API - Examples](https://docs.google.com/document/d/1rjZJWE1nXJNOl4i2Qzz1tWmr6iA2vu8OEsIygkwOBN8/edit?usp=sharing)

## MY FAVORITE YOUTUBE CHANNELS
### From Vietnamese
1. [Tôi đi code dạo - Phạm Huy Hoàng - Website Development (Sr. Full-stack WebDev)](https://www.youtube.com/channel/UCdV9tn79v3ecSDpC1AjVKaw)
2. [Data Guy Story - Data (Sr. Data Scientist)](https://www.youtube.com/channel/UCYHKeGCNDpgbof7uPXrEWbQ)
3. [Trung tâm đào tạo tin học Khoa Phạm](https://www.youtube.com/user/khoazend)

### From US/UK-ers:
1. [Web Dev Simplified](https://www.youtube.com/c/WebDevSimplified)
 
### From Indian (Eng Language)
1. [Clever programmer](https://www.youtube.com/channel/UCqrILQNl5Ed9Dz6CGMyvMTQ)

## SOMETHING I LEARNED FROM MY MANAGER, MY LEADER, MY COLLEAGUE
- About setting sring by ' or ": some speacial character such as "\n" can be shown by " and ' is not.
