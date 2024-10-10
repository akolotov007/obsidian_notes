## What is the DOM?
- document object model
	- follows a sort of tree pattern, with nodes having parent/sibling relationships
![[Pasted image 20241004145048.png]]

## Selecting in the DOM

```js
//GetElementById()

const mainTitle = document.getElementById('main-heading');
console.log("Get Element By Id")
console.log(title);

//getElementByClassName()

const listItem = document.getElementsByClassName('list-items');
console.log("Get Element By Class Name 'list-items'")
console.log(listItem);

  
//getElementsbyTagName()

const listItems = document.getElementsByTagName('li');
console.log("Get Element By Tag Name 'li' ")
console.log(listItems);

//querySelector()

// selects the first thing that matches the selector
const container = document.querySelector('div');
console.log("querySelector()")
console.log(container)


//querySelectorAll()

const divs = document.querySelectorAll('div');
console.log("querySelectorAll()");
console.log(divs);
```


## Traversing the DOM

```js
// Parent Node
const ul = document.querySelector('ul');
ul.parentNode 
ul.parentElement


// Child Node
console.log("Child Nodes");
console.log(ul.childNodes[1]);
console.log(ul.firstChild); //#text, not the li
console.log(ul.lastChild);  //#text
// example of using childNodes
ul.childNodes[1].style.backgroundColor = 'blue';

// Easier/Better way to select
console.log(ul.children); //shows the li as you would expect
console.log(ul.firstElementChild);
console.log(ul.lastElementChild);

// Sibling Node
console.log("Sibling Nodes");
console.log(ul.previousElementSibling);
console.log(ul.nextElementSibling);
```

## DOM manipulation
```js
//Styling Elements

const title = document.querySelector('#main-heading');
// applies in line stying / only applies to a single item
title.style.color = 'red';

const listItems = document.querySelectorAll('.list-items');
console.log(listItems);
 listItems.style.fontSize = '5rem'; // nothing happens


listItems.forEach(item => {
item.style.color = 'blue';
item.style.fontSize = '10rem';
});


// Creating Elements
const ul = document.querySelector('ul');
const li = document.createElement('li'); // have to append it

ul.append(li);


// modifying the text
//3 diff ways to pull the text from an element
const firstListItem = document.querySelector('.list-items');
console.log(firstListItem.innerText); // text as show on website 
console.log(firstListItem.textContent); // how text looks in the HTML file, has whitespace and indent
console.log(firstListItem.innerHTML); // how text looks in the HTML file, +^ & tags

// most commonly to be used
li.innerText = 'X-men';



// modifying attributes and classes
//  Attributes
li.setAttribute('id', 'main-heading'); // id = main-heading
li.removeAttribute('id');

console.log(title.getAttribute('id'));

//  Classes
li.classList.remove('list-items') // .list-items class in CSS
li.classList.add('list-items');
console.log(li.classList.contains('list-items')); // true


// removing element(s)
li.remove();



```