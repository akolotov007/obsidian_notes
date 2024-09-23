## **Lists**
Ordered, changeable, allows duplicate
```python
anotherlist = ["abc", 34, True, 40, "male"] # allows diff data types
len(anotherlist)
anotherlist[0:4]
# using List contructor 
thislist = list(("apple","cherry","kiwi"))
print(thislist) # output: ["apple","cherry","kiwi"]
```
#### List Manipulation

``` python
# Index usage
thislist = ["apple", "banana", "cherry"]  

thislist[1] = "blackcurrant" 
	# output: apple, blackcurrant, cherry
thislist[0:2] = ["blossom", "watermelon"]
	# output: blossom, watermelon, cherry
thislist.insert(1,"kiwi")
	# output: blossom, kiwi, watermelon, cherry

# Adding items to a list
blist = ["a","b","c"]
blist.append("d")
	# output: a, b, c, d

alist = [1,2,3]
alist.extend(blist)
	# output: 1,2,3,a,b,c,d
	# can be any other iterable obj (tuple,set,list,dict)

# Removing Items
blist.remove("b") # remove first occurence of item
del blist[2]# at index 
alist.pop(0) # remove at specific index or 
	alist.pop() # remove last item 

# Delete or clear list
del thislist
thislist.clear()
```
#### List Comprehension

```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]  
newlist = [x for x in fruits if "a" in x]  
	# output: apple, banana, mango
print(newlist)

# newlist = [_expression_ for _item_ in _iterable_ if _condition_ == True]
newlist = ['hello' for x in fruits] 
	# output: hello, hello, hello, hello, hello

newlist = [x for x in range(10) if x < 5]
	# output:  [0, 1, 2, 3, 4]

```
#### Sorting Lists

```python
.sort() # sort alphabetically / numerically ascending

thislist = [100, 50, 65, 82, 23]  
thislist.sort()
	#output: [23, 50, 65, 82, 100]

# Sort list descending 
.sort(reverse=True)

# Reverse order of list
.reverse()
```
#### Copy List

```python
# cannot list1 = list2 / will be only a reference to list1, not copy
thislist = ["apple", "banana", "cherry"]
mylist = thislist.copy()
print(mylist)
# OR
thislist = ["apple", "banana", "cherry"]  
mylist = list(thislist)  
print(mylist)

```

#### List Methods

```python
.append() # add element at end
.clear() #clear list
.copy() #returns copy of list
.count() # number of elements w/ specified value
.extend() # add elements of any iterable (list,dict,set) to end 
.index() # index of first element with specified value
.insert() # at specific position
.pop() # removes last, or specific
.remove() # removes with specified value
.reverse() # reverses list
.sort() # sorts list
```

## **Tuples**
ordered, _unchangeable_ , allows duplicate 
```python
tuple1 = ("abc", 34, True, 40, "male") # allows diff data types

# tuple with one item
thistuple = ("apple",) # make sure to add the , 

# tuple constructor 
thistuple = tuple(("apple", "banana", "cherry")) # note the double round-brackets
```

#### Changing Tuple Values
although immutable, workaround by making into list then back into tuple

```python
thistuple = ("apple", "banana", "cherry", "apple", "cherry")  
x = list(thistuple)
x[1] = "pies"
thistuple = tuple(x)
```

#### Tuple Unpacking
```python
fruits = ("apple", "banana", "cherry")
(green, yellow, red) = fruits

# Use * if number of var less than number of values, the remainder assigned to list

fruits = ("apple", "banana", "cherry", "strawberry", "raspberry")  
(green, yellow, *red) = fruits # 3 vars, 5 tuple values 
print(green) # apple
print(yellow) # banana
print(red) # ['cherry', 'strawberry', 'raspberry']
```

## **Sets**
unordered, _items_ unchangeable, unindexed 
```python
myset = {"apple", "banana", "cherry"}
print(myset) # returns random order of set items

```
#### Item Manipulation
```python
thisset = {"apple", "banana", "cherry"}  
for x in thisset:  
  print(x)
	  # random order output
```
##### add/update/remove set items
```python
thisset.add("watermelon")
#
thisset = {"apple", "banana", "cherry"}  
tropical = {"pineapple", "mango", "papaya"}   
thisset.update(tropical) # add items from another interable obj (tuple,list,dict,etc)
#
thisset.remove("apple") 
# thisset.discard("apple") 
```

#### Joining Sets
```python
.union() & .update() # joins items from both sets
.intersection() # keeps ONLY duplicates
.difference() # keeps items from first set that aren't in other set
```
### **Dictionary**
Ordered, changeable, no duplicates

```python
thisdict = {  
  "brand": "Ford",  
  "model": "Mustang",  
  "year": 1964  
}
# Accessing Items
x = thisdict["model"]
x = thisdict.get("model")

# Get Keys / Values
x = thisdict.keys()
x = thisdict.values()

# Get items
x = thisdict.items()
	# dict_items([('brand', 'Ford'), ('model', 'Mustang'), ('year', 1964)])

```
##### Change Items

```python 
thisdict = {  
  "brand": "Ford",  
  "model": "Mustang",  
  "year": 1964  
}  
thisdict["year"] = 2018
	# or
thisdict.update({"year":2020})
```

##### Add/ Remove items
```python 
# Adding
thisdict["color"] = "red" # Added new Key:Value pair
	# or 
thisdict.update({"color":"red"})

# Removing 
thisdict.pop("model") # if empty, last item popped
thisdict.del["model"] # if empty, deletes dictionary
thisdict.clear()
```

##### Copy Dictionaries
```python
some_dict.copy(thisdict)
# or
some_dict = dict(thisdict)
```

#### Nested Dictionaries
```python
myfamily = {  
  "child1" : {  
    "name" : "Emil",  
    "year" : 2004  
  },  
  "child2" : {  
    "name" : "Tobias",  
    "year" : 2007  
  },  
  "child3" : {  
    "name" : "Linus",  
    "year" : 2011  
  }  
} 
# Indexing nested 
myfamily["child2"]["name"]
```

### Methods
Many methods are shared amongst the data types / these are for lists
```python 
.append() # add element at end
.clear() #clear list
.copy() #returns copy of list
.count() # number of elements w/ specified value
.extend() # add elements of any iterable (list,dict,set) to end 
.index() # index of first element with specified value
.insert() # at specific position
.pop() # removes last, or specific
.remove() # removes with specified value
.reverse() # reverses list
.sort() # sorts list
```