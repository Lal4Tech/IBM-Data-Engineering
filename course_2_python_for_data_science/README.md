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

Reusable code block
  
**Built in functions**:

- ```len```: return length of the sequence or collection.
- ```len```: return sum of elements in collection
- ```sorted``` vs ```sort```:
  - ```sorted``` returns a new list. It does not change the original list.
  - ```sort```on the other hand changes the original list and it does not return new list.

**User defined Functions**:

```python
def add1(a):
  """
  add 1 to a
  """
  b = a + 1
  return b

print(add1(3)) ## rint 4
```

Multiple parameters:

```python
def mult(a, b):
  c = a * b
  return c

print(mult(2, 3)) ## print 6
```

Functions without return:

```python
def no_return(s):
  print(s)

no_return("Hello!") # Print Hello!

def no_work():
  pass

no_return() # Print None
```

Collecting arquments: when the number of arguments are unknown for a function, all can be packed into a tuple/dictionary

```python
# Example with tuple
def print_names(*names):
  for name in names:
    print(name)

print_names("Hello", "World", "Python") # in function, names = ("Hello", "World", "Python")
print_names("Hello", "World") # in function, names = ("Hello", "World")
```

```python
# Example with tuple
def printDictionary(**args):
    for key in args:
        print(key + " : " + args[key])

printDictionary(Name='John',State='Hesse',City='Frankfurt')
``````

**Hands-on Lab**: [Functions](labs/9-Functions.ipynb)

### Exception Handling

To catch errors within a program

**try-except statement**:

```python
try:
  f = open("file.txt", "r")
  f.write("File for exception handling!)
except IOError:
  print("Unable to open the file!)
except:
  print"Some other type of error occured!")
```

**try-except-else statement**:

```python
try:
  f = open("file.txt", "r")
  f.write("File for exception handling!)
except IOError:
  print("Unable to open the file!)
else:
  print"The file was written successfully")
```

**try-except-else-finally statement**:

```python
try:
  f = open("file.txt", "r")
  f.write("File for exception handling!)
except IOError:
  print("Unable to open the file!)
else:
  # else allows one to check if there was no exception when executing the try block
  print"The file was written successfully")
finally:
  # finally allows us to always execute something even if there is an exception or not.
  f.close() 
  print("The file is now closed")
```

**Hands-on Lab**: [Exceptions](labs/10-Excecption.ipynb)

### Objects and Classes

In Python everything(int, float, str, boolean, list, tuple, set, dict etc) is an object.

- Every Object has:
  - a type
  - an internal data representation(blueprint)
  - a set of procedures(methods) to interact with object.
- An object is an instance of a particular type.
- A class has
  - Data attributes
  - Methods
- Objects are instances of class
  
Example:

```python
class Circle(object): # define class, here the attribute object represent the parent class
    # function __init__ is a special method(constructor) used to initialize data attributes
    def __init__(self, radius, color):
      # self parameter represent newly created instance of class
      # data attributes(parameters) used to initialize each instance of the class
      self.radius = radius
      self.color = color

    def add_radius(self, r):
      # method to add radius
      self.radius = self.radius + r

# Create an object of class Circle
c = Circle(10, "blue")

# Access the object attribute values
print(c.radius) # will print 10

# Change the object attribute value
c.color = "red"

# Call method
c.add_radius(8)
```

```dir(<name of object>)``` can be used ot list the attribute and methods associated with class.

**Hands-on Lab**: [Classes](labs/11-Classes.ipynb)

**Hands-on Lab**: [Text Analysis](labs/12-Text_Analysis.ipynb)

<hr style="border:2px solid gray">

## Working with Data in Python

### File Operations

**Reading files**:

```python
# f is the file object, first parameter is file name and second parameter is the mode: r-read, w-write, a-append
f = open("file_name", "r") 

print(f.name) # will print the file name. here 'file_name'
print(f.mode) # will print the file mode. here 'r'

f.close() # to close the file object
```

Use ```with``` statement for open the file as it automatically closes the file after operations.

```python
with open("file_name", "r") as f:
  content = f.read()
  print(content)
```

Function ```readline()``` can be used to read one line of a file at a time. ```readlines()``` can be used to read and save lines to a list.

**Hands-on Lab**: [Read file](labs/13-ReadFile.ipynb)

**Writing files**:

```python
with open("file_name", "w") as f:
  f.write("This is line 1\n")
  f.write("This is line 2\n")
```

use mode ```a``` to append to the file instead of over writing.

**Hands-on Lab**: [Write file](labs/14-WriteFile.ipynb)

### Pandas

```python
import pandas as pd
csv_path = 'file.csv'
df = pd.read_csv(csv_path)
df.head()

print(df.ix[0,0]) # access the first-row and first column in the dataframe

df1 = df[df['age'] > 18]
new_file = 'file_new.csv'
df1.to_csv(new_file)

```

**Hands-on Lab**: [Pandas Basics](labs/15-Pandas_Basics.ipynb)

**Hands-on Lab**: [Pandas Load Data](labs/16-Pandas_LoadData.ipynb)

### Numpy

A numpy array(nd-array) is similar to list, but contain data of same type.

```python
import numpy as np
a = np.array([0, 1, 2, 3, 4])

print(a[0]) # output: 0

print(a.size) # output: 5

print(type(a)) # output: numpy.ndarray

print(a.dtype) # to objtain data type of elements. Here, output: dtype('int64')

print(a.ndim) # number of dimensions or rank of the array. Here, output: 1

print(a.shape) # size of the array in each dimension. Here, output: (5,)
```

**indexing and slicing**:

```python
c = np.array([20, 1, 2, 3, 4])

c[0] = 100 # change first element of array to 100

d = c[1:4] # d:array([1, 2, 3])

c[3:5] = 300, 400 # c:array([100, 1, 2, 300, 400])
```

**Basic Operations**:

Vector Addition and Subtraction:

```python
# Without numpy
u = [1, 0]
v = [0, 1]

z = []

for n, m in zip(u, v):
  z.append(n + m)

# With numpy
z = u + v # z:array([1, 1])
```

Product:

```python
# Without numpy
u = [1, 2]
v = [3, 2]

z = []

for n, m in zip(u, v):
  z.append(n * m)

# With numpy
z = u * v # z:array([3, 4])
```

Dot Product:

```python
import numpy as np

# With numpy
z = np.dot(u, v) # z:5
```

Adding constant to a numpy array:

```python
u = np.array([1, 2, 3, -1])
z = u + 1 # z:array([2, 3, 4, 0])
```

**Universal Functions**:

```python
import numpy as np

a = np.array([1, -1, 1, -1])
mean_a = a.mean() # mean_a: 0.0

b = np.array([1, -2, 3, 4, 5])
max_b = b.max() # max_b: 5

np.pi

x = np.array([0, np.pi/2, np.pi])

y = np.sin(x) # y:array([0, 1, 1.2e-16])

np.linspace(-2, 2, num=5) # returns evenly spaced 5 numbers from specified interval. Here [-2, -1, 0, 1, 2]

x = np.linspace(0, 2 * np.pi, 100)
y = np.sin(x)
plt.plot(x, y)
```

**Two Dimensional Numpy**:

```python
a = [[11, 12, 13], [21, 22, 23], [31, 32, 33]]

A = np.array(a)

print(A.ndim) # output: 2

print(A.shape) # output: 3, 3

print(A.size) # output: 9

print(A[0:2, 2]) # output: array([13, 23])

# element-wise addition
x = np.array([[1, 0], [0, 1]])
y = np.array([[2, 1], [1, 2]])
z = x + y # z:array([[3, 1], [1, 3]])

# scalar multiplication
y = np.array([[2, 1], [1, 2]])
z = 2 * y # z: array([[4, 2], [2, 4]])

# element-wise product
x = np.array([[1, 0], [0, 1]])
y = np.array([[2, 1], [1, 2]])
z = x * y # z:array([[2, 0], [0, 2]])

# matrix multiplication
A = np.array([[0, 1, 1], [1, 0, 1]])
B = np.array([[1, 1], [1, 1], [-1, 1]])
Z = np.dot(A, B) # z:array([[0, 2], [0, 2]])
```

**Hands-on Lab**: [One dimensional Numpy Operations](labs/17-Numpy1D.ipynb)

**Hands-on Lab**: [Two dimensional Numpy Operations](labs/18-Numpy2D.ipynb)

<hr style="border:2px solid gray">

## APIs and Data Collection

### Simple APIs

APIs let two pieces of softwares talk to each other.

REST(**RE**presentational **S**tate **T**ransfer) APIs are a type of APIs. They allow us to communicate through internet and leting us to take advantage of resources such as storage.

- Client and Resource(Web services) are end points communicating each other.
- Client find/use the service via *end point*.
- Client request to the resource via end web services send response to the client.
- The request is usually communicated via an *HTTP* message which usually contain a JSON which contain instructions for what operation to be performed.
- API keys are used for identiying the clients and athorize the resources accordingly.
- **PyCoinGecko** API to collect data

```python
!pip install pycoingecko
from pycoingecko import CoinGeckoAPI

cg = CoinGeckoAPI()
bitcoin_data = cg.get_coin_market_chart_by_id(id='bitcoin', vs_currency='usd', days=30)

data = pd.DataFrame(bitcoin_price_data, columns=['TimeStamp', 'Price'])
data['Date'] = pd.to_datetime(data['TimeStamp'], unit='ms')

aggregated_data = data.groupby(data.Date.dt.date).agg({'Price: ['min', 'max', 'first', 'last']})
```

**Hands-on Lab**: [Intro to API](labs/19-Intro_API.ipynb)

### REST APIs, Webscrapping and Working with Files

**HTTP Methods**:

- *GET*: Retrieves data from the server
- *POST*: Submits data to serbver
- *PUT*: Updates ata already on server
- *DELETE*: Deletes data from server

**REST API common status codes**:

- 1XX : Informational
- 100: Everything So Far is OK
- 2XX: Success
- 200: OK
- 3XX: Redirection
- 300: Multiple Choices
- 4XX: Client Error
- 401: Unauthorized
- 403: Forbidden
- 404: Not Found
- 500: Server Error
- 501: Not Implemented

**Get Requests**:

```python
import requests
ur = 'http:/www.ibm.com/'
r = requests.get(url)
print(r.status_code) # if 200: success
print(r.request.headers) # requst headers
prrint(r.headers) # outputs reponse headers
```

request with parameters:

```python
import requests

url_get = 'http://httpbin.org/get'
payload = {"name": "John", "ID": "123"}
r = requests.get(url_get, params=payload)

print(r.url) # Output: 'http://httpbin.org/get?name=John&ID=123'
print(request.body) # Output: None
print(r.text) # Print the content in text
print(r.headers['Content-Type']) # Outputs content type. eg: 'application/json'

print(r.json()) # if the content-type is json, we can format it using json
```

**Post Requests**:

Post request send the data in the request body. Not in request URL.

```python
import requests

url_post = 'http://httpbin.org/post'
payload = {"name": "John", "ID": "123"}
r_post = requests.post(url_post, data=payload)

print(r_post.request.body) # Output: name=John&ID=123
print(r.request.body) # Output: None for the get method

print(r_post.json()['form']) # {'ID': '123', 'name': 'John'}
```

**Hands-on Lab**: [Access REST APIS](labs/20-Requests_HTTP.ipynb)

**Hands-on Lab**: [API Examples](labs/21-API_Examples.ipynb)

**HTML for Webscrapping**:


<hr style="border:2px solid gray">