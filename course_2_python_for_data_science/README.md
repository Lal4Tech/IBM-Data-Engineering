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

<hr style="border:2px solid gray">

## Python Programming Fundamentals

<hr style="border:2px solid gray">

## Working with Data in Python

<hr style="border:2px solid gray">

## APIs and Data Collection

<hr style="border:2px solid gray">