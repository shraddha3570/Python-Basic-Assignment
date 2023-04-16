

```python
1. Why are functions advantageous to have in your programs?
Answer: Functions helps us to reuse the code.It makes code readable and easier to understand
```


```python
2. When does the code in a function run: when it's specified or when it's called?
    
Answer: the code in a function run when it's called
```


```python
3. What statement creates a function?
Answer: def statement defines and creates a function.
```


```python
4. What is the difference between a function and a function call?
Answer:A function consists of the def statement and the code in its def clause.
    A function call is what executes the function, 
    and the function call evaluates to the function’s return value.

```


```python
5. How many global scopes are there in a Python program? How many local scopes?
Answer: One global scope and a local scope is created whenever a function is called.
The global scope is created once the program starts and gets destroyed with the termination of the python program.
Each function in a python program has its own local scope in which all its variables and object names are defined. 
```


```python
6. What happens to variables in a local scope when the function call returns?
Answer: When a function call returns, the local scope is destroyed, and all the variables in it are forgotten.
```


```python
7. What is the concept of a return value? Is it possible to have a return value in an expression?
Answer: he specific value returned from a function is called the return value. 
Yes, it is possible to have a return value in an expression
```


```python
8. If a function does not have a return statement, what is the return value of a call to that function?
Answer:If there is no return statement for a function, its return value is None.
```


```python
9. How do you make a function variable refer to the global variable?
Answer: A global statement will force a variable in a function to refer to the global variable.
```


```python
10. What is the data type of None?
Answer: NoneType
```


```python
11. What does the sentence import areallyourpetsnamederic do?
Answer: It imports a module named areallyourpetsnamederic.
```


```python
12. If you had a bacon() feature in a spam module, what would you call it after importing spam?
Answer: spam.bacon()
```


```python
13. What can you do to save a programme from crashing if it encounters an error?
Answer: We can use try and except clause. Place the line of code that might cause an error in a try and except clause 
```


```python
14. What is the purpose of the try clause? What is the purpose of the except clause?
Answer: The code that could cause an error goes in the try clause.
    The code that executes if an error happens goes in the except clause.First, try clause is executed it means the 
    code between try and except clause. If there is no exception, then only try clause will run, except clause is finished.
    If any exception occured, try clause will be skipped and except clause will run.
```
