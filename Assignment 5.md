

```python
1. What does an empty dictionary's code look like?
Answer: Two curly brackets: {}
```


```python
2. What is the value of a dictionary value with the key 'foo' and the value 42?
Answer:  {'foo': 42}
```


```python
3. What is the most significant distinction between a dictionary and a list?
Answer: Dictionaries are unordered collection of data points. It uses key, value structure to store the values.
        Lists have ordered items
```


```python
4. What happens if you try to access spam['foo'] if spam is {'bar': 100}?
Answer: we get a key error
```


```python
5. If a dictionary is stored in spam, what is the difference between the expressions 'cat' in spam and 'cat' in spam.keys()?
Answer: There is no difference. The in operator checks whether a value exists as a key in the dictionary.
```


```python
6. If a dictionary is stored in spam, what is the difference between the expressions 'cat' in spam and 'cat' in spam.values()?
Answer:
'cat' in spam checks if 'cat' key is presend in dictionary or not.
'cat' in spam.values() check 'cat' value in any of the key of spam.
```


```python
7. What is a shortcut for the following code?
if 'color' not in spam:
spam['color'] = 'black'
Answer: spam = {}
        spam.setdefault('color', 'black')
```


```python
8. How do you "pretty print" dictionary values using which module and function?
Answer: Using pprint.pprint() 
```
