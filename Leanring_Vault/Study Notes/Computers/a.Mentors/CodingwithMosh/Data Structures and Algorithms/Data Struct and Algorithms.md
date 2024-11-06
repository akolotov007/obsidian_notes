*all code in java*
# Part 1: Linear Structures
array, linked list, stacks, queues, hash tables


## Big O Notation
> A mathematical notation that describes the limiting behavior of a function when arguments tends toward a particular value or infinity - Wikipedia

We use big O to describe the performance of an algorithm 

### O(1)
- constant time
```java
public class Main{

	public void log(int[] numbers){
	// O(1)
		System.out.println(numbers[0]);
	}
}
```


representation  
### O(n)
- linear time
- [[Data Struct and Algorithms#Graph Representation|Graph Representation]]
```java
for (int i =0; i<numbers.length;i++)
// O(n)
	System.out.println(numbers[i])
```

```python
for i in numbers[i]:
	print(i) # O(i)
for n in names[n]:
	print(n) # O(n)
#O (n+i) => O(n) // still grows in linear time, can be simplified to just O(n)

# also applies if we had O(1) and O(n) together:
O(1+n) => O(n) # since constant time isn't significant when adding to linear time, ie +1 doesn't matter that much

```

### O(n^2) 
- quadratic time
- [[Data Struct and Algorithms#Graph Representation|Graph Representation]]
```java
// O(n*n) == O(n^2)
for (int first:numbers) //O(n)
	for (int second:numbers) //O(n)
		System.out.println(first + "," + second)
```

lets say we add another for loop prior to this one:
```java

for (int number:numbers) //O(n)
	System.out.println(number);
	
for (int first:numbers) //O(n)
	for (int second:numbers) //O(n)
		System.out.println(first + "," + second)
// O(n + n^2) => O(n^2) 
// since we only need an approx and not an exact value when using Big O, assuming worst case
```

and if we nest another loop inside the double nested, we get a triple nested, and it becomes `O(n^3)`


### O(log n)
[[Data Struct and Algorithms#Graph Representation|Graph Representation]]
- logarithmic time
- binary search is a good example
	- given a list of sorted arrays, find value:
		- look in middle, is smaller or greater than target?
				![[Pasted image 20241020124036.png]]
			- if smaller, look only at the right side
			- repeat division, check value and move accordingly 

*code snippet shown later in course*

### O(2^n)
[[Data Struct and Algorithms#Graph Representation|Graph Representation]]
- Exponential time
- opposite of logarithmic time 

*code snippet will be shown later*

### Graph Representation
![[Pasted image 20241020124419.png]]


### Space Complexity 
- to describe the runtime complexity of our algorithms
	- trade off between saving time and saving space

- always have the input of size `n`, so we don't count it
	- only look at the additional space that we should allocate relative to the input size


```java
public void greet(String[] names){

	// O(1)-v space complexity 
for (int i=0;i<names.length;i++) // i is independent of input, is O(1) const time
	system.out.println("Hi" + names[i]);
}
```

Now what if we add another string array of the same length as the input array 

```java
public void greet(String[] names){

// O(n+1) => O(n)

String[] copy = new String[names.length];
for (int i=0;i<names.length;i++) 
	system.out.println("Hi" + names[i]);
}
```

## Arrays
- stores items sequentially
- static in size, meaning size cannot be changed later on
	- if we wanted to change the size, have to create another array 
		- and copy data from old to new 

- Strength: 
	- very fast to find items based on index
- Weakness:
	- if we don't know what size to make, we might have to add or remove a lot of items, intensive cost

- in Java, integers take 4 bytes of memory ![[Pasted image 20241020125945.png]]
	-  the first address is 100, the second is 104
![[Pasted image 20241020132838.png]]
- best case scenario: if we remove the last item 
	- Deletion: O(1)

![[Pasted image 20241020133142.png]]
- worst case scenario: if we remove the first item, we have to shift the whole array
	- Deletion: O(n)

### Working with Arrays
 
```java
import Java.util.Arrays;
public static void main(String[] args){
	sizeof_array = 3;
	int [] numbers = new int[sizeof_array];
	// empty array
	System.out.println(Arrays.toString(numbers));
	// [0,  0, 0]
}
```

If we want to populate when we declare it:

```java
int[] numbers = {10,20,30};
System.out.println(numbers.length) // 3
```

### Exercise: Building an Array
let's create an array that we can add and remove items, by making it a **class** to call from:
```java
Array numbers = new Array(length:3);
numbers.insert(item:10);
numbers.insert(item:20);
numbers.insert(item:30);
numbers.removeAt();

// also have indexOf, which returns the index of the first instance of (x)

System.out.println(numbers.indexOf(10)); // 0
System.out.println(numbers.indexOf(30)); // 2
```

create an Array class:  (solution)
```java
// array.java
public class Array {
	private int[] items; 
	private int count;
	
	public Array (int length){
		items. new int[length];
	}

	public void insert(int item){
		// if array full, resize it
		if (items.length  == cout){
			// create a new array 
			int [] newItems  = new int[count*2]
			// copy all existing data into new array
			for (int i =0;i<count;i++){
				newItems[i] = items[i];
			}
			// set 'items' to this new array
			items = newItems;

			}
		// add new item at the end of array
		items[count++] = item;
	}

	public void removeAt(int index){
		// validate the index
		if (index < 0 || index >= count){
			throw new IllegalArgumentException();
		}
		// Shift items to left to fill hole
		// [10,20,30,40]
		// rm array[1]
		// 1 <- 2
		// 2 <- 3 
		for (int i = index; i < count; i++){
		items[i] = items [i+1];
		}
		count--;
	}

	public int indexOf (int item){
		// if we find it, return index
		// otherwise return -1
		// best case: O(1) , worst: O(n), consider worst case
		for (int i=0;i<count;i++)
		if (items[i]=item)
			return i;
		return -1;
	}
	
	public void print() {
		for (int i =0;i<count;i++) 
			// have count instead of items.length
			System.out.println(items[i]);
		}

}
```

```java
//main.java

public class Main{
	public static void main(String[] args){
	Array numbers = new Array(Length:3);
	numbers.insert(item:3);
	numbers.insert(item:4);
	numbers.insert(item:5);
	numbers.insert(item:6);
	numbers.insert(item:7);
	numbers.print(); // [3,4,5,6,7]
	numbers.removeAt(3); // [3,4,5,7]

	}
}
```

### Dynamic Arrays
- we just learned how to make a dynamic array, now we'll look into 2 Java implementations of dynamic arrays
	- Vector
		- grows 100% in size
		- synchronized 
			- only a single thread can access it
	- ArrayList
		- grows 50% in size
		- no synchronized

```java
// ArrayList

import java.util.ArrayList;
Public class Main{
	public static void main(String[] args){
		// <Integer> is a wrapper
		ArrayList<Integer> list = new ArrayList<>();
		list.add(10);
		list.add(20);
		list.remove(10);
		list.indexOf(20);
		list.contains(20);
		list.size();
		list.toArray();		
	}
}
```

### Summary
- simplest data structure
- static vs dynamic
	- dynamic arrays exist in Python and JS 
		- grow and shrink automatically
- ArrayList
![[Pasted image 20241020165902.png]]

## Linked Lists
- used to store a list of objects in sequence
	- unlike array, can grow and shrink in size 
![[Pasted image 20241020170110.png]]
 - Lookup
	 -  By Value - O(n)
	 - By index  - O(n)
 - Insert
	 - at beginning : O(1)
	 - at middle: O(n)
	 - at end: O(1)
 - Deletion
	 - at beginning: O(1)
	 - at middle: O(n)
	 - at end: O(n)
	   

### Working with Linked Lists
```java

public static void main (String[] args){
	LinkedList list = new LinkedList();
	list.add(10);
	list.addLast(20);
	list.addFirst(50);
	// 50,10,20
	list.removeFirst;
	list.contains(10);
	list.indexOf(50);
	list.size();
	var array = list.toArray();
}
```


### Building a Linked List 
- 2 hints: 
	-  a nodes class
	- a linked list class
	- node class preferred inside of linked list class

```java
Public class Node{
	private int value;
	private Node next;
}

Public class LinkedList{
	private Node first;
	private Node last;
}
// addFirst
// addLast
// deleteFirst
// deleteLast
// contains
// indexOf
```

Solution:
	addLast

```java
public class LinkedList{
	private class Node {
		private int value;
		private Node next;
		public Node (int num){
			this.value =  num; 
		}
	
	}
	
	private Node first;
	private Node first;
	
	public void addLast(int item) {
		var node  = new Node(item); 
		// our node will never not have a value
		if (first == null) 
			first = last = node;
		else {
			last.next = node;
			last = node;
		}
		
	}

}
```

