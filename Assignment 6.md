

```python
1. What are escape characters, and how do you use them?
Answer: Escape characters represent characters in string values that would otherwise be difficult or 
    impossible to type into code. In Python strings, the backslash " \ " is a special character,
    also called the "escape" character. It is used in representing certain 
    whitespace characters: " \t " is a tab, " \n " is a newline, and " \r " is a carriage return.     
```


```python
2. What do the escape characters n and t stand for?
Answer:  " \n " is a newline," \t " is a tab
```


```python
3. What is the way to include backslash characters in a string?
Answer: A blackslash character can be introduced with double blackslash characters.
```


```python
4. The string "Howl's Moving Castle" is a correct value. 
Why isn't the single quote character in the word Howl's not escaped a problem?
Answer: Because we have used double quotes to mark the beginning and end of the string.
```


```python
5. How do you write a string of newlines if you don't want to use the n character?
Answer: By default print statements add a new line character at the end of the string. We have to use multiline approach.
```


```python
6. What are the values of the given expressions?
'Hello, world!'[1]
'Hello, world!'[0:5]
'Hello, world!'[:5]
'Hello, world!'[3:]
Answer: 'Hello, world!'[1] ----  'e'
        'Hello, world!'[0:5]----'Hello'
        'Hello, world!'[:5] ----- 'Hello'
        'Hello, world!'[3:]----- 'lo, world!'
```


```python
7. What are the values of the following expressions?
'Hello'.upper()
'Hello'.upper().isupper()
'Hello'.upper().lower()
Answer: 'Hello'.upper() --- 'HELLO'
    'Hello'.upper().isupper() --- True
    'Hello'.upper().lower() ---- 'hello'
```


```python
8. What are the values of the following expressions?
'Remember, remember, the fifth of July.'.split()
'-'.join('There can only one.'.split())
Answer: 'Remember, remember, the fifth of July.'.split() ----- ['Remember,', 'remember,', 'the', 'fifth', 'of', 'July.']
        '-'.join('There can only one.'.split()) -----  'There-can-only-one.'
```


```python
9. What are the methods for right-justifying, left-justifying, and centering a string?
Answer: rjust(), ljust(), and center() string methods, respectively
```


```python
10. What is the best way to remove whitespace characters from the start or end?
Answer: The lstrip() and rstrip() methods remove whitespace characters from the left and right ends of a string, respectively
```
