# Python Introduction

## using a print statement

```python
print('hello')
```
---

## Creating and calling a function

```python
def greet_mark():
	print("hello")
	print("How are you")

def greet_brook():
	print("greet")
	print("book")


greet_mark()
greet_brook()

```
---

## Passing a value to a function

```python
def get_name(name):
	print("hello" + " " + name)
	print("How are you")

get_name('jeril')

```
---

## Built in functions in python

```python

https://docs.python.org/3/library/functions.html

# example: abs() -> returns absolute value. Absolute value of -5 is 5

exNum1 = -5
exNum2 = 5

print(abs(exNum1))

```
---

## Loops in Python

### For loop 

To print each element in a

a = ["banana", "apple", "microsoft"]

for element in a:
	print(element)

### If statemet

x = 5
y =8

if x>y:
	print('x')

