# Datatypes

## Boolean

```python
>>> a = True
>>> b = False
>>> c = True
>>> c == a
True
>>> c and a
True
>>> a and b
False
>>> a or b
True
```

## Float

```python
>>> x = 1.2
>>> x + x
2.4
>>> 3 * x
3.6
>>> x / 3
0.4
>>> x ** 2
1.44
```

## Integer

```python
>>> n = 1
>>> n + 2
3
```

*Note that integer division in Python 2 gives rounded answers.*

```python
>>> n / 3
0
```

## String

```python
>>> s = 'This is a sentence.'
>>> s + s
'This is a sentence.This is a sentence.'
>>> s.replace('is', 'was')
'This was a sentence.'
```

## List

*Python indexing starts at zero.*

```python
>>> l = [1, 2, 3, 4]
>>> l[0]
1
>>> l.index(3)
2
```

List's can hold any type:

```python
things = ['block', 1, 1.0, [1, 2]]
```

## Dictionaries

```python
>>> d = {'first': 'This is the first sentence.', 'second': 'This is the second sentence.'}
>>> d['first']
'This is the first sentence.'
>>> d['third'] = 'This is the third sentence.'
>>> d
{'first': 'This is the first sentence.', 'second': 'This is the second sentence.', 'third': 'This is the third sentence'}
```

# Printing

```python
>>> print(1)
1
>>> print('{} children are at school'.format(5))
5 children are at school
>>> print('line one\nline two')
line one
line two
```

# Conditionals

*Indentation matters! Indent four spaces in blocks.*

```python
>>> x = True
>>> if x == True:
...     print('x is true!')
... elif x == False:
...     print('x is not true!')
... else:
...     print('I do not know what x is!')
...
x is true!
```

# Loops

## For

*Indentation matters! Indent four spaces.*

```python
>>> for number in [1, 2, 3, 4]:
...     print(number)
...
1
2
3
4
```

Maybe you need the index too:

```python
>>> for i, number in enumerate([1, 2, 3, 4]):
...     print('{}: {}'.format(i, number))
...
0: 1
1: 2
2: 3
3: 4
```

## While

*Indentation matters! Indent four spaces.*

```python
>>> n = 0
>>> while n < 3:
...     print(n)
...     n = n + 1
...
0
1
2
```

# Functions

*Indentation matters! Indent four spaces.*

```python
>>> def add(first, second):
...     return first + second
...
>>> add(1, 2)
3
>>> add([1, 2], [3, 4])
[1, 2, 3, 4]
```

# Imports

```python
>>> from math import cos
>>> cos(0.0)
1.0
>>> import math
>>> math.cos(0.0)
1.0
>>> math.sin(0.0)
0.0
```

# User Input

```python
>>> name = raw_input('Please type your name, followed by the enter key:\n')
Please type your name, followed by the enter key:
Jason
>>> print(name)
Jason
```
