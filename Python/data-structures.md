## Array Data Structures

list
: lists are implemented as dynamic arrays behind the scenes.
: This means a list allows elements to be added or removed, and the list will automatically adjust the backing store that holds these elements by allocating or releasing memory.

```python
>>> arr = ["one", "two", "three"]
>>> arr[0]
'one'

>>> # Lists have a nice repr:
>>> arr
['one', 'two', 'three']

>>> # Lists are mutable:
>>> arr[1] = "hello"
>>> arr
['one', 'hello', 'three']

>>> del arr[1]
>>> arr
['one', 'three']

>>> # Lists can hold arbitrary data types:
>>> arr.append(23)
>>> arr
['one', 'three', 23]
```

tuple
: tuple objects are immutable. This means elements can’t be added or removed dynamically—all elements in a tuple must be defined at creation time.

```python
>>> arr = ("one", "two", "three")
>>> arr[0]
'one'

>>> # Tuples have a nice repr:
>>> arr
('one', 'two', 'three')

>>> # Tuples are immutable:
>>> arr[1] = "hello"
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'tuple' object does not support item assignment

>>> del arr[1]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'tuple' object doesn't support item deletion

>>> # Tuples can hold arbitrary data types:
>>> # (Adding elements creates a copy of the tuple)
>>> arr + (23,)
('one', 'two', 'three', 23)
```

string
: String objects are space efficient because they’re tightly packed and they specialize in a single data type. If you’re storing Unicode text, then you should use a string. Because strings are immutable in Python, modifying a string requires creating a modified copy. The closest equivalent to a mutable string is storing individual characters inside a list

```python
>>> arr = "abcd"
>>> arr[1]
'b'

>>> arr
'abcd'
```

## Dictionaries, Maps, and Hash Tables

Dictionary (dict)
: a central data structure. Dicts store an arbitrary number of objects, each identified by a unique dictionary key.

```python
>>> phonebook = {
...     "bob": 7387,
...     "alice": 3719,
...     "jack": 7052,
... }

>>> squares = {x: x * x for x in range(6)}

>>> phonebook["alice"]
3719

>>> squares
{0: 0, 1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

Python includes a specialized dict subclass that remembers the insertion order of keys added to it: collections.OrderedDict

```python
>>> import collections
>>> d = collections.OrderedDict(one=1, two=2, three=3)

>>> d
OrderedDict([('one', 1), ('two', 2), ('three', 3)])

>>> d["four"] = 4
>>> d
OrderedDict([('one', 1), ('two', 2),
             ('three', 3), ('four', 4)])

>>> d.keys()
odict_keys(['one', 'two', 'three', 'four'])
```
