

```python
1. Make a class called Thing with no contents and print it. Then, create an object called example from this class
and also print it. Are the printed values the same or different?
Answer:
class Thing:
    pass
print(Thing)
 <class '__main__.Thing'>
example = Thing()
print(example)
 <__main__.Thing object at 0x0000017930039CA0>
```


```python
2. Create a new class called Thing2 and add the value 'abc' to the letters class attribute. Letters should be printed.
Answer:
class Thing2:
    letters = "abc"
    
print(Thing2.letters)
abc

```


```python
3. Make yet another class called, of course, Thing3. This time, assign the value 'xyz' to an instance (object)
attribute called letters. Print letters. Do you need to make an object from the class to do this?
Answer:
class Thing3:
    def __init__(self):
        self.letters = 'xyz'
print(Thing3.letters)   
AttributeError                            Traceback (most recent call last)
<ipython-input-1-74d69f6d7148> in <module>()
      2     def __init__(self):
      3         self.letters = 'xyz'
----> 4 print(Thing3.letters)

AttributeError: type object 'Thing3' has no attribute 'letters'

something = Thing3()
print(something.letters)
xyz

```


```python
4. Create an Element class with the instance attributes name, symbol, and number. 
Create a class object with the values 'Hydrogen,' 'H,' and 1.
Answer:
class Element:
    def __init__(self, name, symbol, number):
        self.name = name
        self.symbol = symbol
        self.number = number
        
obj = Element('Hydrogen','H',1)
obj.name
'Hydrogen'
```


```python
5. Make a dictionary with these keys and values: 'name': 'Hydrogen', 'symbol': 'H', 'number': 1.
Then, create an object called hydrogen from class Element using this dictionary.
Answer:
dict = {'name':'Hydrogen', 'symbol':'H','number': 1}
hydrogen = Element(**dict) # using dictionary unpacking **
hydrogen.symbol
'H'
hydrogen.name
'Hydrogen'
hydrogen.number
1

```


```python
6. For the Element class, define a method called dump() that prints the values of the object’s attributes
(name, symbol, and number). Create the hydrogen object from this new definition and use dump() to print its attributes.
Answer:
class Element:
    def __init__(self,name,symbol,number):
        self.name = name
        self.symbol = symbol
        self.number = number
    def dump(self):
        print(self.name,self.symbol,self.number)

hydrogen = Element('Hydrogen','H',1)
hydrogen.dump()
Hydrogen H 1
```


```python
7. Call print(hydrogen). In the definition of Element, change the name of method dump to __str__, 
create a new hydrogen object, and call print(hydrogen) again.
Answer:
class Element:
    def __init__(self,name,symbol,number):
        self.name = name
        self.symbol = symbol
        self.number = number
    def __str__(self):
        return ('name=%s, symbol=%s, number=%s'% (self.name, self.symbol, self.number))

hydrogen = Element('Hydrogen','H',1)
print(hydrogen)
name=Hydrogen, symbol=H, number=1
```


```python
8. Modify Element to make the attributes name, symbol, and number private. 
Define a getter property for each to return its value.
Answer:

class Element:
    def __init__(self, name, symbol, number):
        self.__name = name
        self.__symbol = symbol
        self.__number = number
    @property
    def name(self):
        return self.__name
    @property
    def symbol(self):
        return self.__symbol
    @property
    def number(self):
        return self.__number
    
hydrogen = Element('Hydrogen','H',1)
hydrogen.name
'Hydrogen'
hydrogen.symbol
'H'
hydrogen.number
1
```


```python
9. Define three classes: Bear, Rabbit, and Octothorpe. For each, define only one method: eats(). 
    This should return 'berries' (Bear), 'clover' (Rabbit), or 'campers' (Octothorpe).
    Create one object from each and print what it eats.
Answer:
class Bear:
    def eats(self):
        return 'berries'
class Rabbit:
    def eats(self):
        return 'clover'
class Octothorpe:
    def eats(self):
        return 'campers'
    
b = Bear()
r = Rabbit()
o = Octothorpe()
print(b.eats())
berries
print(r.eats())
clover
print(o.eats())
campers
```


```python
10. Define these classes: Laser, Claw, and SmartPhone. Each has only one method: does(). 
    This returns 'disintegrate' (Laser), 'crush' (Claw), or 'ring' (SmartPhone).
    Then, define the class Robot that has one instance (object) of each of these.
    Define a does() method for the Robot that prints what its component objects do.
Answer:
class Laser:
    def does(self):
        return "disintegrate"

class Claw:
    def does(self):
        return "crush"
    
class Smartphone:
    def does(self):
        return "ring"
    
class Robot:
    def __init__(self):
        self.laser = Laser()
        self.claw = Claw()
        self.smartphone = Smartphone()
    def does(self):
        return ('Laser is %s, Claw is %s, SmartPhone is %s' % (self.laser.does(),self.claw.does(),self.smartphone.does()))
    
robo = Robot()
robo.does()
'Laser is disintegrate, Claw is crush, SmartPhone is ring'

```
