# 100+ Python challenging programming exercises
### Content
**1. [Level Description](https://github.com/WenJoy001/Python-programming-exercises#1level-description)**

**2. [Problem Template](https://github.com/WenJoy001/Python-programming-exercises#2problem-template)**

**3. [Questions](https://github.com/WenJoy001/Python-programming-exercises#3questions)**

* [Questions 1-10](https://github.com/WenJoy001/Python-programming-exercises#question-1---level-1)
* [Questions 11-20](https://github.com/WenJoy001/Python-programming-exercises#question-1---level-11)
* [Questions 21-30](https://github.com/WenJoy001/Python-programming-exercises#question-1---level-21)
* [Questions 31-40](https://github.com/WenJoy001/Python-programming-exercises#question-1---level-31)

## 1.   Level Description
- **Level 1 Beginner**  means someone who has just gone through an introductory Python course. He can solve some problems with 1 or 2 Python classes or functions. Normally, the answers could directly be $
- **Level 2 Intermediate** means someone who has just learned Python, but already has a relatively strong programming background from before. He should be able to solve problems which may involve 3 or 3 $
- **Level 3 Advanced** One should use Python to solve more complex problem using more rich libraries functions and data structures and algorithms. He is supposed to solve the problem using several Python$

## 2.   Problem template

- Question
- Hints
- Solution

## 3.   Questions


### Question 1 - Level 1

**Question**:

Write a program which will find all such numbers which are divisible by 7 but are not a multiple of 5,
between 2000 and 3200 (both included).
The numbers obtained should be printed in a comma-separated sequence on a single line.

**Hints**:

Consider use `range(#begin, #end)` method

**Solution**:
``` python
l = []
for i in range(2000, 3201):
    if (i%7 == 0) and (i%5 != 0):
        l.append(str(i))

print ','.join(l)
```
***

### Question 2 - Level 1

**Question**:

Write a program which can compute the factorial of a given numbers.
The results should be printed in a comma-separated sequence on a single line.

Suppose the following input is supplied to the program:
`8`.
Then, the output should be:
`40320`.

**Hints**:

In case of input data being supplied to the question, it should be assumed to be a console input.

**Solution**:
``` python
def fact(x):
    if x == 0:
        return 1
    return x * fact(x - 1)

x = int(raw_input())
print fact(x)
```
***

### Question 3 - Level 1

**Question**:

With a given integral number n, write a program to generate a dictionary that contains `(i, i*i)` such that is an integral number between 1 and n (both included). and then the program should print the `dict`.

Suppose the following input is supplied to the program:
`8`.

Then, the output should be:
`{1: 1, 2: 4, 3: 9, 4: 16, 5: 25, 6: 36, 7: 49, 8: 64}`.


**Hints**:

In case of input data being supplied to the question, it should be assumed to be a console input.
Consider use `dict()`

**Solution**:

``` python
n = int(raw_input())
d = dict()
for i in range(1,n+1):
    d[i] = i*i

print d
```
***

### Question 4 - Level 1

**Question**:

Write a program which accepts a sequence of comma-separated numbers from console and generate a list and a tuple which contains every number.

Suppose the following input is supplied to the program:
`34,67,55,33,12,98`.
Then, the output should be:

```
['34', '67', '55', '33', '12', '98']
('34', '67', '55', '33', '12', '98')
```

**Hints**:

In case of input data being supplied to the question, it should be assumed to be a console input.
`tuple()` method can convert list to tuple

**Solution**:
``` python
values = raw_input()
l = values.split(",")
t = tuple(l)
print l
print t
```
***

### Question 5 - Level 1

**Question**:

Define a class which has at least two methods:
- `getString`: to get a string from console input
- `printString`: to print the string in upper case.

Also please include simple test function to test the class methods.

**Hints**:

Use `__init__` method to construct some parameters

**Solution**:
``` python
class InputOutString(object):
    def __init__(self):
        self.s = ""

    def getString(self):
        self.s = raw_input()

    def printString(self):
        print self.s.upper()

strObj = InputOutString()
strObj.getString()
strObj.printString()
```
***
### Question 6 - Level 2

**Question**:

Write a program that calculates and prints the value according to the given formula:
`Q = Square root of [(2 * C * D)/H]`
Following are the fixed values of C and H:
`C is 50. H is 30`.
D is the variable whose values should be input to your program in a comma-separated sequence.
>**Example**
>
>Let us assume the following comma separated input sequence is given to the program:
`100,150,180`
The output of the program should be:
`18,22,24`

**Hints**:

If the output received is in decimal form, it should be rounded off to its nearest value. 
For example, in case of input data being supplied to the question, it should be assumed to be a console input.

**Solution**:
``` python
#!/usr/bin/env python
import math
c = 50
h = 30
value = []
items = [x for x in raw_input().split(',')]
for d in items:
    value.append(str(int(round(math.sqrt(2*c*float(d)/h)))))

print ','.join(value)
```
***

### Question 7 - Level 2

**Question**:

Write a program which takes 2 digits, X,Y as input and generates a 2-dimensional array. The element $
Note: i=0,1.., X-1; j=0,1,¡­Y-1.
>**Example**:
>Suppose the following inputs are given to the program:
3,5
Then, the output of the program should be:
`[[0, 0, 0, 0, 0], [0, 1, 2, 3, 4], [0, 2, 4, 6, 8]]`

**Hints**:

Note: In case of input data being supplied to the question, it should be assumed to be a console inp$

**Solution**:
``` python 
input_str = raw_input()
dimensions = [int(x) for x in input_str.split(',')]
rowNum = dimensions[0]
colNum = dimensions[1]
multilist = [[0 for col in range(colNum)] for row in range(rowNum)]

for row in range(rowNum):
    for col in range(colNum):
        multilist[row][col] = row * col

print multilist
```
***

### Question 8 - Level 2

**Question**:

Write a program that accepts a comma separated sequence of words as input and prints the words in alphabet order.

Suppose the following input is supplied to the program:
`without,hello,bag,world`.
Then, the output should be:
`bag,hello,without,world`.

**Hints**:

In case of input data being supplied to the question, it should be assumed to be a console input.

**Solution**:
``` python
items = [x for x in raw_input().split(',')]
items.sort()
print ','.join(items)
```
***

### Question 9 - Level 2

**Question**:

Write a program that accepts sequence of lines as input and prints the lines after making all characters uppercase.

Suppose the following input is supplied to the program:
```
Hello world
Practice makes perfect
```
Then, the output should be:
```
HELLO WORLD
PRACTICE MAKES PERFECT
```

**Hints**:

In case of input data being supplied to the question, it should be assumed to be a console input.

**Solution**:
``` python
lines = []
while True:
    s = raw_input()
    if s:
        lines.append(s.upper())
    else:
        break;

for sentence in lines:
    print sentence
```
***

### Question 10 - Level 2

**Question**:

Write a program that accepts a sequence of whitespace separated words as input and prints the words in alphabet order.

Suppose the following input is supplied to the program:
`hello world and practice makes perfect and hello world again`.
Then, the output should be:
`again and hello makes perfect practice world`.

**Hints**:

In case of input data being supplied to the question, it should be assumed to be a console input.
We use set container to remove duplicated data automatically and then use `sorted()` to sort the data.

**Solution**:
```python
s = raw_input()
words = [word for word in s.split(" ")]
print " ".join(sorted(list(set(words))))
```
***

### Question 11 - Level 2

**Question**:

Write a program which accepts a sequence of comma separated 4 digit binary numbers as its input and $
>Example:
Write a program which accepts a sequence of comma separated 4 digit binary numbers as its input and $
\
>Example:
`0100,0011,1010,1001`.
Then the output should be:
`1010`.
\
Notes: Assume the data is input by console.

**Hints**:

In case of input data being supplied to the question, it should be assumed to be a console input.

**Solution**:
```python
value = []
items = [x for x in raw_input().split(',')]
for p in items:
    intp = int(p, 2)
    if not intp%5:
        value.append(p)

print ','.join(value)
```
***


