

```python
1. What exactly is []?
Answer: The empty list value, which is a list value that contains no items.
```


```python
2. In a list of values stored in a variable called spam, how would you assign the value 
'hello' as the third value? (Assume [2, 4, 6, 8, 10] are in spam.)
Answer : spam[2] = "hello"
```


```python
Let's pretend the spam includes the list ['a', 'b', 'c', 'd'] for the next three queries.
3. What is the value of spam[int(int('3' * 2) / 11)]?
Answer: 'd'
```


```python
4. What is the value of spam[-1]?
Answer: 'd'
```


```python
5. What is the value of spam[:2]?
Answer: ['a', 'b']
```


```python
Let's pretend bacon has the list [3.14, 'cat,' 11, 'cat,' True] for the next three questions.
6. What is the value of bacon.index('cat')?
Answer: 1
```


```python
7. How does bacon.append(99) change the look of the list value in bacon?
Answer: [3.14, 'cat', 11, 'cat', True, 99]
```


```python
8. How does bacon.remove('cat') change the look of the list in bacon?
Answer: [3.14, 11, 'cat', True, 99]
```


```python
9. What are the list concatenation and list replication operators?
Answer: The operator for list concatenation is +, while the operator for replication is *.
```


```python
10. What is difference between the list methods append() and insert()?
Answer: Here append( ) will add values only to the end of a list, insert( ) can add them anywhere in the list.

```


```python
11. What are the two methods for removing items from a list?
Answer: The del statement and the remove( ) list method are two ways to remove values from a list.
```


```python
12. Describe how list values and string values are identical.
Answer: Both lists and strings can be passed to len( ), they have indexes and slices,can be used in for loops, 
    can be concatenated or replicated, and can be used with the in and not in operators.

```


```python
13. What's the difference between tuples and lists?
Answer: Lists are mutable so they can have values added, removed, or changed.
    Tuples are immutable so they cannot be changed at all. Also, tuples are written using parentheses (  ),
    while lists use the square brackets [  ].

```


```python
14. How do you type a tuple value that only contains the integer 42?
Answer: a=(42,)
```


```python
15. How do you get a list value's tuple form? How do you get a tuple value's list form?
Answer: Using the tuple() and list() functions
    eg: 
a = [1,2,3]
print(tuple(a))
b = (1,2,3)
print(list(b))
```


```python
16. Variables that "contain" list values are not necessarily lists themselves. Instead, what do they contain?
Answer: Variables do not store values directly.Python variables work with references to objects representing the values.
eg:
a = [1,2,3]
Python creates a new reference for a to point at the object representing the value [1,2,3] in the memory.

```


```python
17. How do you distinguish between copy.copy() and copy.deepcopy()?
Answer: The copy.copy() function will do a shallow copy of a list, while the copy.deepcopy() function will do a deep copy of a list.
```
