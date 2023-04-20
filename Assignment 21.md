

```python
1. Add the current date to the text file today.txt as a string.
Answer:
import datetime
from datetime import date
now = date.today()
cur_date = now.isoformat()
cur_date
'2023-04-20'
with open('today.txt','w') as file:
    file.write(cur_date)
```


```python
2. Read the text file today.txt into the string today_string
Answer:
with open('today.txt','r') as file:
    today_string = file.read()
today_string

'2023-04-20'
```


```python
3. Parse the date from today_string.
Answer:
from datetime import datetime
format = '%Y-%m-%d'
datetime.strptime(today_string,format)
datetime.datetime(2023, 4, 20, 0, 0)
```


```python
4. List the files in your current directory
Answer:
import os
os.listdir('.')
```


```python
5. Create a list of all of the files in your parent directory (minimum five files should be available).
Answer:
import os
os.listdir('..')

['Admin', 'All Users', 'Default', 'Default User', 'desktop.ini', 'Public']
```


```python
6. Use multiprocessing to create three separate processes. Make each one wait a random number of seconds between one
and five, print the current time, and then exit.
Answer:
import multiprocessing

def printsec(seconds):
    from datetime import datetime
    from time import sleep
    sleep(seconds)
    print('wait', seconds, 'seconds, time is', datetime.utcnow())
    
if __name__ == '__main__':
    import random    
    for n in range(3):
        seconds = random.random()
        proc = multiprocessing.Process(target=printsec, args=(seconds,))
        proc.start()
```


```python
7. Create a date object of your day of birth.
my_birthdate = date(1995,3,9)
my_birthdate
datetime.date(1995,3,9)
```


```python
8. What day of the week was your day of birth?
Answer:
my_birthdate.weekday()
3
```


```python
9. When will you be (or when were you) 10,000 days old?
Answer:
from datetime import timedelta
day10000 = my_birthdate + timedelta(days=10000)
day10000
datetime.date(2022, 7, 25)
```
