

```python
1. Create an assert statement that throws an AssertionError if the variable spam is a negative integer.
Answer:
import pyinputplus as pyip
spam = pyip.inputNum(" Enter positive number :")
assert spam > 0
print(spam,'is a positive number')

Enter positive number :-1

 AssertionError                            Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_18384/2550353909.py in <module>
          2 
          3 spam = pyip.inputNum(" Enter positive number :")
    ----> 4 assert spam > 0
          5 print(spam,'is a positive number')
    

    AssertionError:
```


```python
2. Write an assert statement that triggers an AssertionError if the variables eggs and bacon contain strings
that are the same as each other, even if their cases are different (that is, 'hello' and 'hello' are considered the same,
and 'goodbye' and 'GOODbye' are also considered the same).

Answer: 

eggs='Hello'
bacon ='hello'

assert eggs.lower() != bacon.lower() or eggs.upper() != bacon.upper()
print('The eggs and bacon variables are not the same!')

AssertionError                            Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_18384/2374175613.py in <module>
          2 bacon ='hello'
          3 
    ----> 4 assert eggs.lower() != bacon.lower() or eggs.upper() != bacon.upper()
          5 print('The eggs and bacon variables are not the same!')
    

    AssertionError: 
```


```python
3. Create an assert statement that throws an AssertionError every time.
Answer:

assert False ->  this always triggers an exception
assert False
AssertionError                            Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_18384/2103537015.py in <module>
    ----> 1 assert False
    

    AssertionError: 
```


```python
4. What are the two lines that must be present in your software in order to call logging.debug()?
Answer: 
import logging

logging.basicConfig(level=logging.DEBUG, format=' %(asctime)s - %(levelname)s - %(message)s')

```


```python
5. What are the two lines that your program must have in order to have logging.debug() 
send a logging message to a file named programLog.txt?
Answer: 
import logging as lg
lg.basicConfig(filename='programLog.txt', level=lg.DEBUG, format=' %(asctime)s - %(levelname)s - %(message)s')
```


```python
6. What are the five levels of logging?
Answer:
Five level of loggins are DEBUG, INFO, WARNING, ERROR, and CRITICAL
logging.debug() - variable's state and small details
logging.info() - general events, confirm a program is working
logging.warning() - potiental problem to work on in the future
logging.error() - record an error that caused program to fail to do something
logging.critical() - fatal error that has caused
```


```python
7. What line of code would you add to your software to disable all logging messages?
Answer:
logging.disable(level) -> Disables all logging calls of severity 'level' and below. set level = logging.CRITICAL 
since CRITICAL being the highest level , every other level loggings will be disabled.
```


```python
8.Why is using logging messages better than using print() to display the same message?
Answer:
You can disable logging messages without removing the logging function calls. 
You can selectively disable lower-level logging messages. 
You can create logging messages. Logging messages provides a timestamp.

```


```python
9. What are the differences between the Step Over, Step In, and Step Out buttons in the debugger?
Answer:
Step in button will move the debugger into a function call. 
Over button will quickly execute the function call without stepping into it. 
Out button will quickly execute the rest of the code until it steps out of the function it currently is in.
```


```python
10.After you click Continue, when will the debugger stop ?
Answer:
It will stops at next breakpoint, if there are no further breakpoints program will be fully executed.

```


```python
11. What is the concept of a breakpoint?
Answer:
A breakpoint is a setting on a line of code that causes the debugger to pause when the program execution reaches the line.

```
