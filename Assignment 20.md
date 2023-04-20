

```python
1. Set the variable test1 to the string 'This is a test of the emergency text system,' and save test1 to a file
named test.txt.
Answer:
test1 = 'This is a test of the emergency text system'
outfile = open('test.txt', 'wt')
outfile.write(test1)
outfile.close()
```


```python
2. Read the contents of the file test.txt into the variable test2. Is there a difference between test 1 and test 2?
Answer:
with open('test.txt', 'rt') as infile:
    test2 = infile.read()
test2
 'This is a test of the emergency text system'
test1 == test2
True

```


```python
3. Create a CSV file called books.csv by using these lines:
title,author,year
The Weirdstone of Brisingamen,Alan Garner,1960
Perdido Street Station,China Miéville,2000
Thud!,Terry Pratchett,2005
The Spellman Files,Lisa Lutz,2007
Small Gods,Terry Pratchett,1992
Answer:
import csv
rows =[ ['title','author','year'],
    ['The Weirdstone of Brisingamen','Alan Garner',1960],
    ['Perdido Street Station','China Miéville',2000],
    ['Thud!','Terry Pratchett',2005],
    ['The Spellman Files','Lisa Lutz',2007],
    ['Small Gods','Terry Pratchett',1992]]
with open('books.csv','w',newline='') as file:
    writer = csv.writer(file)
    writer.writerows(rows)
```


```python
4. Use the sqlite3 module to create a SQLite database called books.db, and a table called books with these fields: 
    title (text), author (text), and year (integer).
Answer:
import sqlite3
db = sqlite3.connect('books.db')
curs = db.cursor()
curs.execute('create table books(title varchar(20),author varchar(20), year int)')

<sqlite3.Cursor at 0x1f68d5bd180>

db.commit()
```


```python
5. Read books.csv and insert its data into the book table.
Answer:
import pandas as pd
read_books = pd.read_csv('books.csv',encoding='unicode_escape')
read_books.to_sql('books', db, if_exists='append', index = False)
```


```python
6. Select and print the title column from the book table in alphabetical order.
Answer:
curs.execute('select title from books order by title asc')
print(curs.fetchall())
[('Perdido Street Station',), ('Perdido Street Station',), ('Perdido Street Station',), ('Small Gods',),
 ('Small Gods',), ('Small Gods',), ('The Spellman Files',), ('The Spellman Files',), ('The Spellman Files',), 
 ('The Weirdstone of Brisingamen',), ('The Weirdstone of Brisingamen',), ('The Weirdstone of Brisingamen',), 
 ('Thud!',), ('Thud!',), ('Thud!',)]
```


```python
7. From the book table, select and print all columns in the order of publication.
Answer:
curs.execute('select title, author,year from books order by year')
df = pd.DataFrame(curs.fetchall(), columns=['title','author','year'])
df

```


```python
8. Use the sqlalchemy module to connect to the sqlite3 database books.db that you just made in exercise 6.
Answer:
import sqlalchemy
engine = sqlalchemy.create_engine("sqlite:///books.db")
rows = engine.execute('select * from books')
for i in rows:
    print(i)
    
('The Weirdstone of Brisingamen', 'Alan Garner', 1960)
('Perdido Street Station', 'China Miéville', 2000)
('Thud!', 'Terry Pratchett', 2005)
('The Spellman Files', 'Lisa Lutz', 2007)
('Small Gods', 'Terry Pratchett', 1992)
('The Weirdstone of Brisingamen', 'Alan Garner', 1960)
('Perdido Street Station', 'China Miéville', 2000)
('Thud!', 'Terry Pratchett', 2005)
('The Spellman Files', 'Lisa Lutz', 2007)
('Small Gods', 'Terry Pratchett', 1992)
('The Weirdstone of Brisingamen', 'Alan Garner', 1960)
('Perdido Street Station', 'China Miéville', 2000)
('Thud!', 'Terry Pratchett', 2005)
('The Spellman Files', 'Lisa Lutz', 2007)
('Small Gods', 'Terry Pratchett', 1992)
```


```python
9. Install the Redis server and the Python redis library (pip install redis) on your computer. 
Create a Redis hash called test with the fields count (1) and name ('Fester Bestertester'). 
Print all the fields for test.
Answer:
!pip install redis
import redis conn = redis.Redis() conn.delete('test') 1 conn.hmset('test', {'count': 1, 'name': 'Fester Bestertester'}) True conn.hgetall('test') {b'name': b'Fester Bestertester', b'count': b'1'}
```


```python
10. Increment the count field of test and print it.
Answer:
conn.hincrby('test', 'count', 3) 4 conn.hget('test', 'count') b'4'
```
