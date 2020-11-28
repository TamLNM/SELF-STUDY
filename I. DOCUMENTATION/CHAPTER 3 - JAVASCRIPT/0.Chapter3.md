# JAVASCRIPT
## I. About the ECMAScript Editions:
- We have about six version of ECMA Script, include ES1 - ES6, with 2 nearest function:
+ ES5: edition in 2009
+ ES6: edition in 2015 - 2018
- Browers support for ES5: Chome ver23, IE ver9*/10, Edge ver10,...
<i>* Internet Explorer 9 does not support ECMAScript 5 "use strict".</i>
<i>Internet Explorer does not support ECMAScript 2015.</i>

## II. ES5 Features
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
### 1. Use strict
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

### 2. Trim: remove space from both sides of a string
```javascript
String.trim();
```

### 3. Array - Is Array: check a variable is array or not
```javascript
Array.isArray();
```
### 4. Array For Each: check a variable is array or not
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

#### 5. Array Map: update value for each element in array:
```javascript
Array.map()
```
* Using example:
```javascript

```

#### 6. Array Filter: filter array elements with condition
```javascript
const arr = [1,2,3,4];
const arr1 = arr.filter(e => e >= 2)
console.log(arr1);
```

#### 7. Array (LAST Index Of): search an element in a array and return the position. In case not find out, it return -1
```javascript
Array.indexOf(element)
Array.lastIndexOf(element)
```
* Using example
```javascript
const arr = ['1', 'abc', '!_fas'];
console.log(arr.indexOf('abc'));
```

#### 8. Array Stringify: convert a JS Object into a string, use in case the developer want to sent data to server
```javascript
JSON.stringify(object)
```
* Using examples for JSON.stringify and JSON.parse()
```javascript
let objData = {
	'name': 'Le Nguyen Minh Tam',
  'age' : 24,
  'sex' : 'male'
};

let strData = JSON.stringify(objData);
console.log(strData);

let initialData = JSON.parse(strData);
console.log(initialData);
```

#### 9. Object Functions:
...

##### Different functions (I think it's not common)
- Array.reduce()
- Array.reduceRight()
- Array.every()
- Array.some()
- Date.now()

## III. ES6 Features
`... updating ...`

## IV. Let in JS:
- ES2015 introduced two important new JavaScript keywords: let and const.
- For <b>Block Scope</b> variables and constants in Javascript
- We have two different scopes: <b>Global Scope</b> and <b>Function Scope</b>
### 1. About affectly variables scope
#### a. Global scope: which declared in the outside any function position: 
Examples:
```javascript
var name = "Le Nguyen Minh Tam";
// ---> code here can use name <---
function myFunction() {
  // ---> code here can also use name <----
}
```
##### b. Function Scrope: which declared locally
Examples:
```javascript
// ---> code here CAN'T use name <---
function myFunction() {
  var name = "Le Nguyen Minh Tam";
  // ---> code here can also use name <----
}
// ---> code here CAN'T use name <---
```
##### c. Block scope: is the space inside (and between) {}
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

#### d. Redeclared variables:
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
#### e. Redeclared variables:
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
#### f. Using window.<variable>:
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

#### g. Delared with var and let.<variable>:
  > var (allowed) -> var (allowed)/ var (allowed) -> { var (allowed) }
  > let (allowed) -> let (NOT allowed)
  > let (allowed) -> let (allowed)/ let (allowed) -> { let (allowed) }
  > var (allowed) -> let (NOT allowed) -> { var (allowed) -> let (NOT allowed) }
  > let (allowed) -> var (NOT allowed) -> { let (allowed) -> var (NOT allowed) } 
  > not (let, var) -> ... -> var (allowed)
  > not (let, var) -> ... -> let (NOT allowed)

#### h. Const in javascript:
- Scope: block scope.
- With the type of variables are primitive (includes: string, number, boolean, null and undefined), we can change the value of variables when declared with const.
- With the type of variables are reference (include object, array or function) we can change the attributes of this variable.

## V. FormData in HTML5:
### 1. Initialize the FormData in HTML5
3 common ways to initialize a formdata with Javascript:
```javascript
var formData = new FormData();
var formData = new FormData(document.getElementById('formID'));
var formData = new FormData($('form#formID')[0]);
```
### 2. Append:
<b>Purpose:</b> Attach data to DataForm:
```javascript
formData.append(<key>, <value>);
```

### 3. Entries:
<b>Purpose:</b> Convert data to type that developer can read or console log
```javascript
formData.append(name, value);
formData.append(name, value, filename);
```
Usage examples:
```javascript
let formData = new FormData();
formData.append('name', 'Le Nguyen Minh Tam');
formData.append('age', 24);

for(pair of formData.entries()){
  console.log(pair[0] + ", " + pair[1])
}
```

### 4. Values:
<b>Purpose:</b> similar than <b>Entries</b> function, but just return the value of element
```javascript
fromData.value();
```

### FUNCTION THAT I THINK IT'S NOT COMMON IN USE:
- delete
- get 
- getAll
- has
- key
- set



##### *. ABBREVIATIONS + TERMINOLOGY
1. EMCA (in EMCAScript): stands for "European Computer Manufacturer's Association". Can understand like ECMAScript is the modal in build on paper and javascript is the programming language to make it in computer to feel more easily.
