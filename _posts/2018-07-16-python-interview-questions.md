### Python 3 Interview Questions Part 1

#### Question 1

What will be the output of the following code :
```python
print(type(type(int)))
```
**Anwser: <class 'type'>**

**Explanation:** The type() function returns the class of the argument the object belongs to. Thus, type(int) returns which is of the type ‘type’ object.

#### Question 2

What is the output of the following code :
```python
L = ['a','b','c','d']
print ("".join(L))
```
**Anwser: abcd**

**Explanation:** “” depicts a null string and the join function combines the elements of the list into a string. The method **join()** returns a string in which the string elements of sequence have been joined by str separator.
Following is the syntax for join() method −. The join() method takes iterable – objects capable of returning its members one at a time. Some examples are List, Tuple, String, Dictionary and Set
```python
str.join(sequence)
```
#### Question 3

What is the output of the following segment :
```python
chr(ord('A'))
```
**Anwser: A**

**Explanation:** ord() function converts a character into its ASCII notation and chr() converts the ASCII to character.

#### Question 4

What is the output of the following program :
```python
y = 8
z = lambda x : x * y
print(z(6))
```
**Anwser: 48**

**Explanation:** lambdas are concise functions and thus, result = 6 * 8

#### Question 5

What is called when a function is defined inside a class?

**Anwser: Method**

#### Question 6

Which of the following is the use of id() function in python?

**Anwser: Id returns the identity of the object**

**Explanation:** Each object in Python has a unique id. The id() function returns the object’s id. Return the “identity” of an object. This is an integer which is guaranteed to be unique and constant for this object during its lifetime. Two objects with non-overlapping lifetimes may have the same id() value.
```python
id(y)
```

#### Question 7

Suppose list1 is [3, 4, 5, 20, 5, 25, 1, 3], what is list1 after list1.pop(1)?
```python
y = 8
z = lambda x : x * y
print(z(6))
```
**Anwser: [3, 5, 20, 5, 25, 1, 3]**

**Explanation:** pop(i) removes the ith index element from the list. Remove the item at the given position in the list, and return it. If no index is specified, a.pop() removes and returns the last item in the list. (The square brackets around the i in the method signature denote that the parameter is optional, not that you should type square brackets at that position. You will see this notation frequently in the Python Library Reference.)

#### Question 8

time.time() returns ________
```python
print(time.time())
```
**Anwser: the current time in milliseconds since midnight**

**Explanation:** Return the time in seconds since the epoch as a floating point number. The specific date of the epoch and the handling of leap seconds is platform dependent. On Windows and most Unix systems, the epoch is January 1, 1970, 00:00:00 (UTC) and leap seconds are not counted towards the time in seconds since the epoch. This is commonly referred to as Unix time. To find out what the epoch is on a given platform, look at gmtime(0).
