# Python for Data Science, AI & Development

## Python Basics

### Types

- ```type(11)```: ```int```
- ```type(21.213)```: ```float```
- ```type("Hello World")```: ```str```
- ```type(True)```: ```bool```

**Type cast**:

- ```float(2)```: ```2.0```
- ```int(1.1)```: ```1```
- ```int('1')```: ```1```
- ```ìnt('A')```: ```Error```
- ```int(True)```: ```1```
- ```int(False)```: ```0```
- ```bool(1)```: ```True```
- ```bool(0)```: ```False```
  
### Expressions and Variables

**Expressions**:

- ```3 + 4 + 7```: ```14``` (here ```+``` is operator and numbers are operands)
- ```5 - 6```: ```-1```
- ```5 * 6```: ```30```
- ```25 / 5```: ```5.0```
- ```25 / 6```: ```4.166..```
- ```25 // 6```: ```4``` (Integer division)
- ```2 * 60 + 30```: ```150```
- ```30 + 2 * 60```: ```150```
- ```(30 + 2) * 60```: ```1920```

**Variables**:

- ```my_variable = 1```; my_variable:1
- ```my_variable = 10``` (now the value of the variable is changed to 10)
- ```x = 40 + 100 + 50```; x:150
- ```y = x / 10```; y:15.0
- ```x = x / 15```; x:10.0

**Hands-on Lab**: [First python Notebook](labs/1-Write_your_first_python_code.ipynb)

### String Operations

- String is a sequence of characters(alphabets, numbers, spaces, special characters) contained wthin single/double quotes. ```name = Michael Jackson```
- Can access each character using its index.
  - ```name[0]```: ```M```
  - ```name[1]```: ```i```
  - ```name[-1]```: ```n```
- String slicing:
  - ```name[0:4]```: ```Mich```
  - ```name[8:12]```: ```Jack```
  - ```name[::2]```: ```McalJcsn```
  - ```name[0:5:2]```: ```Mca```
- Get length of String - ```len(name)```: ```15```
- Concatenate the string with other - ```statement = name + " is the best"```: ```Michael Jackson is the best```
- Multiply the string with integer - ```3 * "Michael"```: ```Michael Michael Michael```
- String is Immutable - ```name[2]="J"``` is not possible
- Escape sequences
  - ```\n```: new line
  - ```\t```: tab
  - if want to use backslash in the string, use ```\\``` - ```print("Michael Jackson \\ is the best")```: ```Michael Jackson \ is the best```
  - String methods
    - Since string is a sequence, can apply methods work on sequences such as list and tuples.
    - Also have methods specific to String typed
    - ```a = "Hello World"```
    - ```b = a.upper()```; b: ```HELLO WORLD```
    - ```b = a.replace('World', 'Python')```; b: ```Hello Python```
    - ```name.find('el')```: ```5```, ```name.find('Jack')```: ```8```
    - ```name.find('%4A')```: ```-1```; if not found will return ```-1```

**Hands-on Lab**: [Strings](labs/2-Strings.ipynb)

<hr style="border:2px solid gray">

## Python Data Structures

### List and Tuples

**Tuples**:

- Tuples are ordered sequences
- eg: ```ratings = (7, 8, 4, 5, 9, 10)```
- Different type of values in a tuple is possible: ```t = ('world', 12, 5.3)```; ```type(t)```: ```tuple```
- Elements can be accessed by index.
  - ```t[0]```: ```world```
  - ```t[-1]```: ```5.3```
- Concatenating
  - ```t = t + ('python', 3.10)```
  - ```print(t)```: ```('world', 12, 5.3, 'python', 3.10)```
- Slicing
  - ```t[0:3]```: ```('world', 12, 5.3)```
  - ```len(t)```: ```5```
- Tuples are immutable - ```t[2]=99``` is not possible
- Nesting
  - ```x = (1, 4, ("Hello", "World"), 3.4, ("Python", (3, 10)))```
  - ```x[2]```: ```("Hello", "World")```
  - ```x[4][1]```: ```(3, 10)```

**Hands-on Lab**: [Tuples](labs/3-Tuples.ipynb)

**Lists**:
- Lists are ordered sequences
- eg: ```l = ['Hello world', 2, 1.4]```
- Concatenating, Slicing and Nesting are possible(similar to tuples)
- Lists are mutable
  - ```l[0] = "Hello Python"```
  - ```l.extend(['python', 3.10])```: ```['Hello Python', 2, 1.4, 'python', 3.10]```
  - ```l.append(['python', 3.10])```: ```['Hello Python', 2, 1.4, ['python', 3.10]]```
  - ```del(l[0])```: ```[2, 1.4, ['python', 3.10]]```
- Convert String to List
  - ```"Hello World".split()```: ```["Hello", "World"]```
  - ```"a,b,c,d"```: ```['a', 'b', 'c', 'd']```
- If we asign list variable to another and try to change the element, then it will affect both variable as both variable referencing the same list. Cloning th3e variable can be used in this to solve this.
  - ```a = ["Hello python", 3, 10.0]```
  - ```b = a[:]```
  - Now if we change a, b will not change

**Hands-on Lab**: [Lists](labs/4-Lists.ipynb)

### Dictionaries

- Key-value pairs
- Kyes have to be immutable and unique
- Values can be immutable, mutable and duplicates
- eg: ```dict = {'a': 1, 'b': 'hello', c: 3.4}```
- ```dict['b']```: ```'hello'```
- Add new value to the list - ```dict['d'] = 78```
- To delete - ```del(dict['c'])```
- To check if a key in dictionary - ```'b' in dict```: ```True```, ```'x' in dict```: ```False```
- To get all keys in the dictionary - ```dict.keys()``` and to get values - ```dict.values()```

**Hands-on Lab**: [Dictionaries](labs/5-Dictionaries.ipynb)

### Sets

- Unordered, mutable collection of different type of unique objects
- eg: ```s = {1, "hello", (4, 9.5), "hello"}```: ```{1, "hello", (4, 9.5)}``` (duplicat elements will be removed)
- Convert list to set
  - ```a_list = [1, 4, 6, 4]```
  - ```a_set = set(a_list)```
  - ```a_set```: ```{1, 4, 6}```
- Set Operations
  - ```s = {"Hello World", "Python", 3.10}```
  - Add element - ```s.add("Programming")```
  - Remove element - ```s.remove("Programming")```
  - Check if an element in set - ```"Programming" in s```: ```False```
  - Mathematical operations
    - ```s1 = {1, 5, 6, 8}```, ```s2 = {2, 5, 6, 9}```
    - ```s1 & s2```: ```{5, 6}``````
    - ```s1.union(s2)```: ```{1, 5, 6, 8, 2, 9}```
    - ```s1.issubset(s2)```: ```False```

**Hands-on Lab**: [Sets](labs/6-Sets.ipynb)

<hr style="border:2px solid gray">

## Python Programming Fundamentals

### Conditions and Branching

**Comparison Operators**:

- ```==```
- ```!=```
- ```>```
- ```<```
- ```>=```
- ```<=```

Examples:

- ```a = 6```
- ```a == 7```: ```False```
- ```a >= 5```: ```True```
- ```"Hello" == "World"```: ```False```

**Branching**:

if-else statement:

```python
if (age > 18):
  print("Welcome")
else:
  print("Move on!)
```

elif statement:

```python
if (age > 18):
  print("Welcome")
elif(age == 18):
  print("Please go to School :D")
print("Move on")
```

**Logic Operators**:

- ```and```
- ```or```
- ```not```

```python
year = 2000

if ((year < 2000) and (year > 1990)):
  print("Album was made in 90's")
else:
  print("Album was not made in 90's")
```

**Hands-on Lab**: [Conditions](labs/7-Conditions.ipynb)

### Loops

- range function
  - ```range(3)```: ```[0, 1, 2]```
  - ```range(10, 14)```: ```[10, 11, 12, 13]```

```for``` loop:

```python
for i in range(5):
  print(i ** 2)
```

```python
l = [1, 3, 8]
for idx, item in enumerate(l):
  print(idx, item)
```

```while``` loop:

```python
i = 0
while i < 10:
  print(i)
  i+=1
```

**Hands-on Lab**: [Loops](labs/8-Loops.ipynb)

### Functions

### Exception Handling

### Objects and Classes

<hr style="border:2px solid gray">

## Working with Data in Python

<hr style="border:2px solid gray">

## APIs and Data Collection

<hr style="border:2px solid gray">