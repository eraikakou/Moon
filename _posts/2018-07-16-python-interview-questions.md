<p> Python 3 Interview Questions Part 1 </p>

### __***Question 1***__

What will be the output of the following code :
```python
print(type(type(int)))
```
**Anwser: <class 'type'>**

**Explanation:** The type() function returns the class of the argument the object belongs to. Thus, type(int) returns which is of the type ‘type’ object.

### __***Question 2***__

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
### __***Question 3***__

What is the output of the following segment :
```python
chr(ord('A'))
```
**Anwser: A**

**Explanation:** ord() function converts a character into its ASCII notation and chr() converts the ASCII to character.

### __***Question 4***__

What is the output of the following program :
```python
y = 8
z = lambda x : x * y
print(z(6))
```
**Anwser: 48**

**Explanation:** lambdas are concise functions and thus, result = 6 * 8

### __***Question 5***__

What is called when a function is defined inside a class?

**Anwser: Method**

### __***Question 6***__

Which of the following is the use of id() function in python?

**Anwser: Id returns the identity of the object**

**Explanation:** Each object in Python has a unique id. The id() function returns the object’s id. Return the “identity” of an object. This is an integer which is guaranteed to be unique and constant for this object during its lifetime. Two objects with non-overlapping lifetimes may have the same id() value.
```python
id(y)
```

### __***Question 7***__

Suppose list1 is [3, 4, 5, 20, 5, 25, 1, 3], what is list1 after list1.pop(1)?
```python
list1 = [3, 4, 5, 20, 5, 25, 1, 3]
list1.pop(1)
print(list1)
```
**Anwser: [3, 5, 20, 5, 25, 1, 3]**

**Explanation:** pop(i) removes the ith index element from the list. Remove the item at the given position in the list, and return it. If no index is specified, a.pop() removes and returns the last item in the list. (The square brackets around the i in the method signature denote that the parameter is optional, not that you should type square brackets at that position. You will see this notation frequently in the Python Library Reference.)

### __***Question 8***__

time.time() returns ________
```python
print(time.time())
```
**Anwser: the current time in milliseconds since midnight**

**Explanation:** Return the time in seconds since the epoch as a floating point number. The specific date of the epoch and the handling of leap seconds is platform dependent. On Windows and most Unix systems, the epoch is January 1, 1970, 00:00:00 (UTC) and leap seconds are not counted towards the time in seconds since the epoch. This is commonly referred to as Unix time. To find out what the epoch is on a given platform, look at gmtime(0).

### __***Question 9***__

What is the output of the following code :

```python
print (9//2)
print (9/2)
```
**Anwser: 4 4.5**

**Explanation:** The ‘//’ operator in Python returns the integer part of the floating number.

### __***Question 10***__

Which function overloads the >> operator?

**Anwser: rshift**

**Explanation:** rshift() overloads the >> operator. >> Binary Right Shift The left operand's value is moved right by the number of bits specified by the right operand.

**Logical right shift one bit:**


![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/6/64/Rotate_right_logically.svg/210px-Rotate_right_logically.svg.png)

### __***Question 11***__

Which operator is overloaded by the or() function?

**Anwser: | **

**Explanation:** or() function overloads the bitwise OR operator. 
Python Bitwise Operators
Bitwise operator works on bits and performs bit-by-bit operation. Assume if a = 60; and b = 13; Now in binary format they will be as follows −

a = 0011 1100

b = 0000 1101

-----------------

a&b = 0000 1100 [& Binary AND]

a`|`b = 0011 1101 [`|` Binary OR]

a^b = 0011 0001 [^ Binary XOR]

~ a = 1100 0011 [~ Binary Ones Complement] 

Binary Left/RIght Shift

### __***Question 12***__

What is the output of the following program :
```python
i = 0
while i < 3:
       print(i)
       i++
       print (i+1)
```
**Anwser: Error**

**Explanation:** There is no operator ++ in Python

### __***Question 13***__

What is the output of the following program :
```python
print ("Hello World"[::-1])
print ("Hello World"[::])
```
**Anwser: dlroW olleH, Hello World**

**Explanation:** [::] depicts extended slicing in Python and [::-1] returns the reverse of the string.

### __***Question 14***__

Given a function that does not return any value, what value is shown when executed at the shell?

**Anwser: None**

**Explanation:** Python explicitly defines the None object that is returned if no value is specified.

### __***Question 15***__

Which module in Python supports regular expressions?

**Anwser: re**

**Explanation:** re is a part of the standard library and can be imported using: import re.

### __***Question 16***__

What is the output of the following program :
```python
print( 0.1 + 0.2 == 0.3)
```
**Anwser: False**

**Explanation:** Neither of 0.1, 0.2 and 0.3 can be represented accurately in binary. The round off errors from 0.1 and 0.2 accumulate and hence there is a difference of 5.5511e-17 between (0.1 + 0.2) and 0.3.

### __***Question 17***__

Which of the following is not a complex number?

**Anwser: k = 2 + 3l**

**Explanation:** l (or L) stands for long.

### __***Question 18***__

Given a string s = “Welcome”, which of the following code is incorrect?
- print s[0]
- print s.lower()
- s[1] = ‘r’
- print s.strip()

**Anwser:  s[1] = ‘r’**

**Explanation:** strings are immutable in Python.

