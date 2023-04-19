

```python
1. Create a list called years_list, starting with the year of your birth, and each year thereafter until the year 
of your fifth birthday. For example, if you were born in 1980. the list would be 
years_list = [1980, 1981, 1982, 1983, 1984, 1985].

Answer:
years_list = [i for i in range(1982,1982+6)]
years_list
```


```python
2. In which year in years_list was your third birthday? Remember, you were 0 years of age for your first year.
Answer:
years_list[3]
1985
```


```python
3.In the years list, which year were you the oldest?
Answer:
max(years_list)
1987
```


```python
4. Make a list called things with these three strings as elements: "mozzarella", "cinderella", "salmonella".
Answer:
things = list(['mozzarella', 'cinderella','salmonella'])
things
['mozzarella', 'cinderella', 'salmonella']
```


```python
5. Capitalize the element in things that refers to a person and then print the list. Did it change the element in the list?
Answer:
Capitalize() will not update the list original values.
Answer:

for i in things:
    print(i.capitalize())
things  
Mozzarella
Cinderella
Salmonella
['mozzarella', 'cinderella', 'salmonella']
```


```python
6. Make a surprise list with the elements "Groucho," "Chico," and "Harpo."
Answer:
surprise_list = ["Groucho", "Chico", "Harpo"]
surprise_list
['Groucho', 'Chico', 'Harpo']
```


```python
7. Lowercase the last element of the surprise list, reverse it, and then capitalize it.
Answer:
surprise_list[-1].lower()
'harpo'
surprise_list[-1][::-1]
'opraH'
surprise_list[-1][::-1].upper()
'OPRAH'

```


```python
8. Make an English-to-French dictionary called e2f and print it. Here are your starter words: dog is chien, cat is chat,
and walrus is morse.
Answer:
e2f = {'dog': 'chien', 'cat': 'chat', 'walrus': 'morse'}
e2f 
{'dog': 'chien', 'cat': 'chat', 'walrus': 'morse'}
```


```python
9. Write the French word for walrus in your three-word dictionary e2f.
Answer:
e2f['walrus']
'morse'
```


```python
10. Make a French-to-English dictionary called f2e from e2f. Use the items method.
Answer:
f2e = dict((key,value) for value,key in e2f.items())
f2e
{'chien': 'dog', 'chat': 'cat', 'morse': 'walrus'}

```


```python
11. Print the English version of the French word chien using f2e.
Answer:
f2e['chien']
'dog'
```


```python
12. Make and print a set of English words from the keys in e2f.
Answer:
e2f.keys()
dict_keys(['dog', 'cat', 'walrus'])
```


```python
13. Make a multilevel dictionary called life. Use these strings for the topmost keys: 'animals', 'plants', and 'other'. 
    Make the 'animals' key refer to another dictionary with the keys 'cats', 'octopi', and 'emus'.
    Make the 'cats' key refer to a list of strings with the values 'Henri', 'Grumpy', and 'Lucy'.
    Make all the other keys refer to empty dictionaries.
    
Answer:
life ={'animals':{'cat':['Henri', 'Grumpy', 'Lucy'], 'octopi':'', 'emus':''},
       'plants' :'',
       'other' :'' }
life
{'animals': {'cat': ['Henri', 'Grumpy', 'Lucy'], 'octopi': '', 'emus': ''},
 'plants': '',
 'other': ''}

```


```python
14. Print the top-level keys of life.
Answer:
life.keys()
dict_keys(['animals', 'plants', 'other'])

```


```python
15. Print the keys for life['animals'].
Answer:
life['animals'].keys()
dict_keys(['cat', 'octopi', 'emus'])
```


```python
16. Print the values for life['animals']['cats']
Answer:
life['animals']['cat']
['Henri', 'Grumpy', 'Lucy']
```
