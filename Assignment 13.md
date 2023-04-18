

```python
1. What advantages do Excel spreadsheets have over CSV spreadsheets?
Answer:
-Using large files is much easier in Excel for the end user. Also, you can have additional functions like selecting
individual cells for import, convert dates and time automatically, reading formulas and their results, filters, sorting, etc
-In excel, data can also be stored in form of charts and graphs
-In Excel, spreadsheets can have values of data types other than strings; cells can have different fonts, sizes, or
color settings; cells can have varying widths and heights; adjacent cells can be merged
-Excel not only stores data but can also do operations on the data
```


```python
2.What do you pass to csv.reader() and csv.writer() to create reader and writer objects?
Answer:
We pass a File object, obtained from a call to open().
import csv
aFile = open('example.csv')
areader = csv.reader(aFile)
aData = list(areader)
aData
```


```python
3. What modes do File objects for reader and writer objects need to be opened in?
Answer:
File objects need to be opened in read-binary ('rb') for Reader objects and write-binary ('wb') for Writer objects
```


```python
4. What method takes a list argument and writes it to a CSV file?
Answer:
writerow() method
```


```python
5. What do the keyword arguments delimiter and line terminator do?
Answer:
delimiter argument changes the string used to separate cells in a row. 
lineterminator argument changes the string used to separate rows.
```


```python
6. What function takes a string of JSON data and returns a Python data structure?
Answer:
json.loads()
```


```python
7. What function takes a Python data structure and returns a string of JSON data?
Answer:
json.dumps()
```
