## background
 - JS runs in the browser via a JS engine
	 - Firefox: SpiderMonkey
	 - Chrome: V8
 - Ryan Dahl: took the open source JS engine in chrome and embedded it in a C++ program
	 - creator of Node.JS
	 - allows to run JS outside of the browser

Difference btwn JS and ECMAscript?
 - ECMA - specification 
 - JS - programming language

It is best practice to put scripts after the body of an HTML document
- since file is read from top to bottom by computer
## Beginning

### Primitives types

```js
<script src = "index.js"></script>
// linking script 

// creating var
let name = 'Mosh';
console.log(name);
// is camel case


// constant
const interestRate = 0.3;
console.log(name);

// Primitive Data types
/* 
string		let name = 'Mosh'
number		let age = 30;
boolean		isApproved = false;
undefined	firstName = undefined;
null 		selectedColor = null;
*/
```

### Static vs Dynamic Typing
- #### Static typed 
	- when declaring a var, the type of the var is set and **cannot** be changed
- #### Dynamic Typed
	- when declaring the var, the type of the var **can** be changed at runtime

```js
let name = 'Andre'
typeof(name) // string
name = 1;
typeof(name) // number
```

### Reference Types

```js
//Object

let person = {
	name: 'Mosh',
	age: 30
}
// 2 ways to access the properties of obj
//Dot notation
person.name = 'John'

//Bracket Notation
person['name'] = 'Mary'

console.log(person.name) // Mary
```

```js
//Array

let selectedColors = ['red', 'blue'];
selectedColors[2] = 'green'; // red, blue, green
selectedColors[2] = 1; // red, blue, 1 
```

```js
// functions

function greet(name, lastName){
console.log('hello' + name + lastName)
}

greet("Andre", 'Lopez');
```

### DOM (Document Object Model) Manipulation

```js
// Adding elements to a page
const body = document.body;
body.append("Hello World", " Bye");

// Creating elements
const div = document.createElement('div');
// created element, but haven't added it to the page
div.innerText = "Hello World";
body.append(div);

```

#### .textContent  vs .innerText

```html
<body>
	<div>
		<span>Hello</span>
		<span style = "display:none;">Bye</span>
	</div>
</body>
```

```js
const div  = document.querySelector("div")
console.log(div.textContent) // shows all the text directly from HTML
console.log(div.innerText) // displays text as its shown on the page


```

#### Modifying HTML element 

```js
const body = document.body;
const div = document.createElement("div")
div.innerHTML = "<strong>Hello World 2</strong>" // .innerHTML / poses security risk. instead:

const strong = document.createElement("strong")
strong.innerText = "Hello World 2"
div.append(strong)
body.append(div)
// breaking up the JS, but making it more secure
```

#### Removing elements from DOM

```html
<div>
	<span id = "hi"> Hello </span> 
	<span id = "bye"> Bye </span>
</div>
```

```js
const body = document.body;
const div = document.querySelector("div")
const spanHi = document.querySelector("#hi")
const spanBye = document.querySelector("#bye")

spanBye.remove() // removing it 
div.append(spanBye) // adding it back

```

##### Modifying Element Attributes

```html
<div>
	<span title = "hello" id = "hi"> Hello </span> 
	<span id = "bye"> Bye </span>
</div>
```

```js
/*const body = document.body;
const div = document.querySelector("div")
const spanHi = document.querySelector("#hi") */

// Getting Attribute 
spanHi.getAttribute('id')
spanHi.getAttribute('title')

// attributes can also be called as methods on the element itself
spanHi.id
spanHi.title

// Setting Attribute
spanHi.setAttribute('id', 'bleh')
spanHi.id = 'bleh'

// Removing Attributes
spanHi.removeAttribute('id')

```
##### Modifying data attributes
```html
<div>
	<span id = "hi" data-test = "this is a test"> Hello </span> 
</div>
```

```js
/*const body = document.body;
const div = document.querySelector("div")
const spanHi = document.querySelector("#hi") */

// Selecting data attribute
console.log(spanHi.dataset.test)

// Creating a new data attribute 
spanHi.dataset.newName = 'heyo!!'

```

##### Modifying Element Classes


```html
<div>
	<span id = "hi" class = "hi1 hi2"> Hello </span> 
</div>
```

```js
// Adding a class
spanHi.classlist.add('new-class') 

// Removing a class
spanHi.classlist.remove('hi1') 

// Toggling a class
spanHi.classlist.toggle('hi2')
// can also add a class that hasn't been assigned yet, such as hi3
spanHi.classlist.toggle('hi3', true) // adds that class 
// can use boolean to toggle

```

##### Modifying Element Style

```js
spanHi.style.color = 'red'
//
spanHi.style.backgroundColor = 'black' // in CSS: 'background-color' => JS: 'backgroundColor'


```


## OOP programming
 - programming paradigm centered around *objects* rather than functions

### Objects
#### Creating 
```js
const circle = 
{
	radius: 1,
	location :
	{
		x:1,
		y:1
	},
	draw: function()
	{
		console.log('draw')
	}
};

circle.draw();
```
#### factories and constructors
What if we want to create multiple circles? 
- that's where factories/constructors come into play

```js
// Factory
function createCircle(radius){
	return {
	radius, // radius: radius <= simplified syntax 
	draw: function(){console.log('draw')}
	}
}
const circle = createCircle(1);
circle.draw();


// Constructor
function Circle(radius) {
	this.radius = radius;
	this.draw = function(){
		console.log('draw');
	}
};
const anotherCircle = new Circle(2); // when using 'new', calls the object. If not, calls in the window scope
```

### Functions are Objects
```js
function Circle(radius) {
	this.radius = radius;
	this.draw = function(){
		console.log('draw');
	}
};
// in console...
Circle.name(); // 'Circle'
Circle.length(); // amount of args
Circle.constructor(); // f Function() {[native code]} 



```

#### Primitives vs Reference Types
- **Primitives / Values**
	- number
	- string
	- boolean
	- symbol (new in es6)
	- undefined 
	- null
- **Reference Types**
	- Object
	- function 
	- array

```js
let x = 10;
let y=x;
x=20;
console.log(x) // 20
console.log(y) // 10
// data was copied from x to y / both are independent of one another

// Now if x was an object
let x = {value:10}
let y = x;
x.value = 20;
console.log(x) // 20
console.log(y) // 20
// 'x' is just a pointer to the object in memory, same as 'y'\
```

*primitives* are copied by their **value**
*objects* are copied by their **reference**

another example
```js
let number = 10;

function increase(num){
num++;
}
increase(number);
console.log(number); // 10
// again, this is showing how primitives are copied by their value, as the 'number' and 'num' are indep of one another   

let OBJ = {value:10};

function increase(obj){
obj.value++;
}
increase(obj);
console.log(obj); // 11
// showing how an object is passed by reference


```

#### Working with properties
objects are dynamic in JS, you can add or delete properties 

```js

function Circle(radius){
	this.radius = radius;
	this.draw = function(){
		console.log('draw')
		}
};
const circle = new Circle(10);

// Dot Notation
circle.location = {x:1};
// Bracket Notation
circle['location'] = {x:1}; // how can this be useful? ^1
// adding a property

// ^1 ... if we want to dynamically access the property name, we can do so with []
const PropertyName = 'center location';
circle[PropertyName] = {x:1};

// Deleting property 
delete circle['location'];
delete circle.location;
```
\
##### Enumerating Properties

``` js
// enumerating all properties 
for (let key in circle){
	if (typeof circle[key] !== 'function'){
	console.log(key, circle[key]);
	}
}
// getting all the keys
// another way / doesn't separate methods and properties
const keys = Object.keys(circle);
console.log(keys);

// check if obj has a property/method
if ('radius' in circle){
	console.log('Circle has a radius.')
}
```

### abstraction
```js
function Circle(radius){
	this.radius = radius;
	//introducing some complexity 
	this.defaultLocation = {x:0, y:0};
	
	// going to call this function inside .draw
	this.computeOptimumLocation = function(){
	}
	this.draw = function(){
	this.computeOptimumLocation();
	console.log('draw')
	} 
} 
const circle = new Circle(10);
// we as the consumer shouldn't be able to have access to this function, therefore we need to hide in it...
circle.computeOptimumLocation();
```


#### Private Properties and Methods
*continuing from the previous example*
If we create a local variable to the function, it will stay inside the function 
	meaning that it isn't a property of the function

```js
function Circle(radius){
	this.radius = radius;
	
	let defaultLocation = {x:0, y:0};
	
	let computeOptimumLocation = function(){
	//...
	};
	
	this.draw = function(){
	computeOptimumLocation();
	// defaultLocation();
	// this.radius;
	console.log('draw')
	} 
};
// we have now made defaultlocation and computeoptimumlocation functions that exist only in the scope of the Circle() function. 
circle.computeOptimumLocation() // will not show
```

### getters / setters
*looking back at previous example*
What if we want to print the default location of the circle without being able to write to it?

```js
function Circle(radius){
	this.radius = radius;

	let defaultLocation = {x:0, y:0};
	
	this.draw = function(){
	console.log('draw')
	} 
	
	// new code
	Object.defineProperty(this, 'defaultLocation', {
		// getter = function used to read a property
		get: function(){
			return defaultLocation;
		},
		// setter = allows to define the property from outside this function
		set: function(value) {
		// can also do validation on the 'value' since we are in a function
			if (!value.x || !value.y)
					throw new Error("Invalid Location.")
			defaultLocation = value;
		}
	});
};
const circle = new Circle(10);
circle.defaultLocation = 1; // throws error

```

### Exercise

create a stopwatch which has 3 methods, start, stop, reset and 1 property - duration
- you cannot call .start more than 1 time
- you cannot all .stop more than 1 time
- duration's default 0
-  

```js
function stopwatch(){
let startTime, endTime, running, duration = 0;

this.start = function(){
	if (running)
		throw new Error('Stopwatch has already started.');
	running = True; 
	startTime = new Date();
};

this.stop = function(){
	if (!running)
		throw new Error('Stopwatch is not started.');
	running = false;

	endTime = new Date();

	const seconds = (endTime.getTime() - startTime.getTime()) / 1000;
	duration += seconds;
};
this.reset = function(){
	startTime = null;
	endTime = = null;
	running = false;
	duration = 0;
	};

Object.defineProperty(this, 'duration' {
	get: funtion() {return duration;}

});

}

```


## ES6 Concepts
####  Let / Constant  / Var
- var = can be reassigned, function declaration // rarely used
- let = can be reassigned ,block scope
- const = cannot be reassigned , block scope
```js
let x=10;
x = 20; 

const y = 30;
y=40; // error
const obj = {key:'value'};
obj.key = 'newValue'; // allowed even though const
```

#### This
- returns a reference to the current object
```js 
const person = {
  name: 'Charlie',
  walk() {console.log(this)};
};

person.walk(); // 'this' returns reference to 'person' object
const walk  = person.walk();
walk(); // 'this' returns the global object (window scope)
``` 

##### Binding 'this'
we can make it so that `this` refers back to the `person` object that we created 
```js
// functions are objects, having their own methods. 
// allows us to call the `.bind` method 
const walk = person.walk.bind(person);
walk(); // 
```

#### Arrow Functions
Arrow functions provide a shorter syntax for writing functions. 
- They also do not have their own `this`, making them ideal for methods that need to maintain the context of their enclosing scope.
```js
// older way
const square = function(number){
	return number*number;
}
// arrow function = newer 
const square = (x) => x * x;
console.log(square(4)); // 16
```

```js
const jobs = [
{id:1, isActive: true},
{id:2, isActive: true},
{id:3, isActive: true},
];
// return the jobs that are passed through a function 
const activeJobs = job.filter(function(job){return job.isActive;}); // one way 
const activeJobs = job.filter(job => job.isActive); // one way 
  
```

##### arrow functions and this
- arrow functions don't rebind the this keyword

#### Objects
ES6 makes working with objects easier. You can create objects with shorthand syntax for properties and methods.
```js
const name = 'Alice';
const age = 25;
const person = { name, age }; // Shorthand for { name: name, age: age }

const greet = function() {
  console.log(`Hello, my name is ${this.name}`);
};

const personWithGreet = {
  name: 'Bob',
  greet,
};

personWithGreet.greet(); // Hello, my name is Bob
```

#### Object De-Structuring
- let's say that we want to grab the properties of an object and store them in separate variables

```js
const address = {
street: '',
city: '',
country: ''
}
// how it usually looks like
const street = address.street;
const city = address.city;
const country = address.country;

// de-constructing
const {street: st, city, country} = address;
	   // alias^ 
```

```js
// Array Destructuring
const arr = [1, 2, 3];
const [a, b] = arr;
console.log(a, b); // 1 2

// Object Destructuring
const person = { name: 'Dave', age: 30 };
const { name, age } = person;
console.log(name, age); // Dave 30

```

#### Array Maps

```js
const colors = ['red', 'green', 'blue'];

// one way
const items = colors.map(function(color){
	return '<li>' + color + '<li>';  
});

// arrow function
	const items = colors.map(color => `<li>${color}</li>`);
										// `` and not single quotes ''
console.log(items);
```



#### spread
[[2. Advanced Concepts#Spread operator|spread operator/Fireship]]
The spread operator (`...`) allows you to expand arrays or objects into individual elements or properties.
```js
const arr1 = [1, 2];
const arr2 = [3, 4];
// old way
const combined = first.concat(second);
// spread operator
const combined = [...arr1,'a' , ...arr2]; // [1, 2, 'a', 3, 4]
	//adding stuff in btwn-^
const clone = [...first];



const obj1 = { a: 1 };
const obj2 = { b: 2 };
const combinedObj = { ...obj1, ...obj2, location = "Australia" }; // { a: 1, b: 2, location = 'Australia' }
```

#### Classes
ES6 introduced a class syntax for creating objects. Classes provide a clear structure for creating objects and inheritance.
```js
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a noise.`);
  }
}
```

##### Inheritance
*extending from previous example*
``` js
class Dog extends Animal {
  speak() {
    console.log(`${this.name} barks.`);
  }
}

const dog = new Dog('Rex');
dog.speak(); // Rex barks
```

*another example*
```js 
class Person {
	constructor(name){
		this.name= name}

	walk(){
		console.log("walking");}
}

class Teacher extends Person {
	constructor(name, degree){
		super(name); // taking the 'name' from the parent // will throw error if not written
		this.degree = degree; // 
	}

	teach() {
		console.log('teach');}
}

const teacher = new Teacher('Mosh', 'MSc');
							// degree ^

```


#### modules
ES6 introduced a module system that allows you to export and import code between different files. This helps in organizing code better.

```js
// inside myModule.js
export const greet = (name) => `Hello, ${name}!`;
// be default, all objects that are defined in a module are private
// to make public, place `export` before them

// main.js
import { greet } from './myModule';
console.log(greet('Alice')); // Hello, Alice!

```

##### named and default exports
- you can export anything via its name, such as classes, functions etc.

```js
//named export
// teacher.js
export function promote {};
// person.js
import {promote} from './teacher.js'
```

you can also create default export as such:
```js
// teacher.js
export default class Teacher extends Person {}

// person.js
import Teacher from './teacher' 
// notice missing {}, since default its not needed
```
`
`default -> import ... from ' '`
`named -> import {...} from ' '`
`both -> import ..., {...} from ' '`

```
```