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

