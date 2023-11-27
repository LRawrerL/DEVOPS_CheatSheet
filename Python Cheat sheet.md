### Main entry point
```python
def main():
	print("This is the main entry point")

if __name__ == '__main__':
	main()
```
- Single entry point which the interpreter will first execute
- Lines 4-5 prevents accidental invokes of the script
### Functions
- Used for [[Software Unit Test]]s
- Scope of a function is limited to current [[Python]] file it is located in
- Can be accessed outside using **imports** 
```python
def my_function():  
  print("Hello from a function")  

def main():
	my_function()

if __name__ == '__main__':
	main()
```
### Data types and Structures 
```python
this_str = "str"
# '' Also acceptable
this_int = 1
this_float = 1.23
this_list = [1,2]
this_tuple = (1,2) // Ordered, cannot change
this_set = {1,2} // Unordered, cannot change
this_Bool = True 
#  bytes is a data type
```
- Used [[Vaulted Modules/Y1S1 IEP/Function|Function]] **type()** to show data type 
- **Returns** a **object** which needs to be **converted** to a **string** if used in a **sentence**
```python
temperature = 38.4 
print(type(temperature))
# float
```
#### Lists
```python
thislist = ["apple", "banana", "cherry"]  
for x in thislist:  
  print(x)
```
### Conditional Statements
- Long hand version
```python
a = 200  
b = 33  
if b > a:  
  print("b is greater than a")  
elif a == b:  
  print("a and b are equal")  
else:  
  print("a is greater than b")
```
- Short hand version
```python
a = 2  
b = 330  
print("A") if a > b else print("B")
```
- If else statements **cannot** be **empty** use the word **pass** to avoid this error
- Pythons logical operators are **and**, **or**, and **not**

### Bit-wise operators
- Used for manipulating binary data
![](https://i.imgur.com/v3xI9iM.png)
### Loops
- For loops
```python
for x in range(2, 6):  
  print(x)
  #returns 2,3,4,5
```
- While loops
```python
i = 1  
while i < 6:  
  print(i)  
  i += 1
  #returns 1,2,3,4,5
```
### Importing packages
- Decompose software project into several projects 
- Use **import** mechanism to allow **functions** from other files to be used in another **python** file
```python
#File name called mymodule.py
def greeting(name):  
  print("Hello, " + name)

person1 = {  
  "name": "John",  
  "age": 36,  
  "country": "Norway"  
}
```
```python
#Seperate File
import mymodule  
  
mymodule.greeting("Jonathan")
```
- Possible to rename a module 
```python
#Seperate File
import mymodule as mx
  
mx.greeting("Jonathan")
```
- Possible to import variables
```python
#Seperate File
import mymodule  
  
a = mymodule.person1["age"]  
print(a)
```

### Using PyTest
```python
# import function from another file
import mymodule

# Define test case to be used
def test():
	result = []
	input = "This is a test"
	result = mymodule.isString(input)
	assert (result == 1)
```

### Dictionaries all in 1
- Used to represent data in a key value pair
- Data type not a **DATABASE** 
- No duplicates
- Ordered
- Changeable 
```python
mydict = {"name" : "yixuan", "age" : 18}
# example of a dictionary
print(len(mydict))
# 1 as 0, 1
```

- Accessing Items in a dictionary
```python
mydict = {"name" : "yixuan", "age" : 18}
print(mydict["name"])
print(mydict.get("name"))
# yixuan
```

- Iterating through a dictionary ways
```python
mydict = {"name" : "yixuan", "age" : 18}
# returning values
for key in mydict:
  print(mydict[key])
# yixuan , 18

# returning keys
for key in mydict:
  print(key)
# name, age
```

- Iterating through a list with dictionaries 
```python
myList = [
	{
		'foo':12,
		'bar':14
	},
	{
		'foo':52,
		'bar':641
	},
	{
		'foo':6,
		'bar':84
	}
]

for dictionary in myList:
	print(dictionary['foo'])
# basically loops through the list, at each index there is a dictionary. The second line will take the 'foo' key and print out its value 

for dictionary in myList:
	for key in dictionary:
      		print(key)
# Prints out each key 

for dictionary in myList:
	for key in dictionary:
      		print(dictionary[key])
# Prints out each value
```