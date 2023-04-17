

```python
1. Is the Python Standard Library included with PyInputPlus?
Answer:PyInputPlus is not a part of the Python Standard Library, we must install it separately using pip
```


```python
2. Why is PyInputPlus commonly imported with import pyinputplus as pypi?
Answer: pypi is alias of PyInputPlus.It saves us from typing pyinputplus each time we want to call a PyInputPlus function
```


```python
3. How do you distinguish between inputInt() and inputFloat()?
Answer: inputInt() : Accepts an integer value, and returns int value
        inputFloat() : Accepts integer/floating point value and returns float value
```


```python
4. Using PyInputPlus, how do you ensure that the user enters a whole number between 0 and 99?
Answer: In the inputint function we can set the min = 0 and max = 99 to ensure user enters number between 0 and 99
```


```python
5. What is transferred to the keyword arguments allowRegexes and blockRegexes?
Answer: The allowRegexes and blockRegexes 
        keyword arguments take a list of regular expression strings to determine what the PyInputPlus function will accept or 
        reject as valid input.
```


```python
6. If a blank input is entered three times, what does inputStr(limit=3) do?
Answer: It will throw RetryLimitException exception.
```


```python
7. If blank input is entered three times, what does inputStr(limit=3, default='hello') do?
Answer: When you use limit keyword arguments and also pass a default keyword argument,
the function returns the default value instead of raising an exception

```
