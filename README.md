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
var obj = JSON.parse(text);
  

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
- Create multiple elements: `<i>element*number_need_create</i>`

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
The place you put the command ```"use strict"``` specified the affected area of strict mode.
Example:
```javascript
"use strict";
function foo(){
    var bar = 0;
    return bar;
}

// Uncaught ReferenceError: bar is not defined
bar = 1;
```
```javascript
function foo(){
    "use strict";
    // Uncaught ReferenceError: bar is not defined
    bar = 0;
    return bar;
}
```
- Inconvinient things in strict mode:
+ Can't use the variables that's not declared (by var/ let)

// This will run normally
bar = 1;

#### b. Trim: remove space from both sides of a string
```javascript
String.trim();
```

#### c. Array - Is Array: check a variable is array or not
```javascript
Array.isArray();
```
#### d. Array For Each: check a variable is array or not
```javascript
Array.forEach()
```
* Using example:
```javascript
let arr = [1,2,3,4];
arr.forEach(element => {
	console.log(element);
});
```
OR you can use:
```javascript
let arr = [1,2,3,4];
arr.forEach(function(element){
	console.log(element);
});
```
OR you can use:
```javascript
let arr = [1,2,3,4];
arr.forEach(myFunction);

function myFunction(){
	console.log(element);
});
```

##### e. Array Map: update value for each element in array:
```javascript
Array.map()
```
* Using example:
```javascript

```

##### f. Array Filter: filter array elements with condition
```javascript
const arr = [1,2,3,4];
const arr1 = arr.filter(e => e >= 2)
console.log(arr1);
```

##### g. Array (LAST Index Of): search an element in a array and return the position. In case not find out, it return -1
```javascript
Array.indexOf(element)
Array.lastIndexOf(element)
```
* Using example
```javascript
const arr = ['1', 'abc', '!_fas'];
console.log(arr.indexOf('abc'));
```

##### h. Array Stringify: convert a JS Object into a string, use in case the developer want to sent data to server
```javascript

```

##### Different functions (I think it's not common)
- Array.reduce()
- Array.reduceRight()
- Array.every()
- Array.some()


### 3. ES6 Features


### 4. JS let:
- ES2015 introduced two important new JavaScript keywords: let and const.
- For <b>Block Scope</b> variables and constants in Javascript
- We have two different scopes: <b>Global Scope</b> and <b>Function Scope</b>
#### a. About affectly variables scope
###### a1. Global scope: which declared in the outside any function position: 
Examples:
```javascript
var name = "Le Nguyen Minh Tam";
// ---> code here can use name <---
function myFunction() {
  // ---> code here can also use name <----
}
```
###### a2. Function Scrope: which declared locally
Examples:
```javascript
// ---> code here CAN'T use name <---
function myFunction() {
  var name = "Le Nguyen Minh Tam";
  // ---> code here can also use name <----
}
// ---> code here CAN'T use name <---
```
###### a3. Block scope: is the space inside (and between) {}
Examples:
- Var:
```javascript
{
  var x = 2;
}
// x CAN be used here
```
- Let
```javascript
{
  let x = 2;
}
// x can NOT be used here
```

##### a4. Redeclared variables:
Examples:
- Ex1:
```javascript
var  x = 10;
// Here x is 10
{  
  var x = 2;
  // Here x is 2
}
// Here x is 2
```
- Ex2:
```javascript
var  x = 10;
// Here x is 10
{  
  let x = 2;
  // Here x is 2
}
// Here x is 10
```
##### a5. Redeclared variables:
Examples:
- Ex1:
```javascript
var i = 5;
for (var i = 0; i < 10; i++) {
  // some statements
}
// Here i is 10
```
- Ex2:
```javascript
let i = 5;
for (let i = 0; i < 10; i++) {
  // some statements
}
// Here i is 5
```
##### a6. Using window.<variable>:
- Ex1:
```javascript
var carName = "Volvo";
// code here can use window.carName

```  
- Ex2:
```javascript
let carName = "Volvo";
// code here cannot use window.carName
```

##### a7. Delared with var and let.<variable>:
  > var (allowed) -> var (allowed)/ var (allowed) -> { var (allowed) }
  > let (allowed) -> let (NOT allowed)
  > let (allowed) -> let (allowed)/ let (allowed) -> { let (allowed) }
  > var (allowed) -> let (NOT allowed) -> { var (allowed) -> let (NOT allowed) }
  > let (allowed) -> var (NOT allowed) -> { let (allowed) -> var (NOT allowed) } 
  > not (let, var) -> ... -> var (allowed)
  > not (let, var) -> ... -> let (NOT allowed)

##### a8. Const in javascript:
- Scope: block scope.
- With the type of variables are primitive (includes: string, number, boolean, null and undefined), we can change the value of variables when declared with const.
- With the type of variables are reference (include object, array or function) we can change the attributes of this variable.

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

## WEBSITES THAT'S USEFUL FOR ME:
1. [HTML Formatter](https://webformatter.com/html)
You can format the code in CSS, Javascript, PHP, JSON in there
2. [JSFiddle - For javascript testing](https://jsfiddle.net/)
3. [DiffChecker - For checking (two file/doc)'s differences](https://www.diffchecker.com/)
*. [TomatoTime](https://tomato-timer.com/)



## SOMETHING I LEARNED FROM MY MANAGERS, MY LEADERS, MY COLLEAGUES
- About setting sring by ' or ": some speacial character such as "\n" can be shown by " and ' is not.
