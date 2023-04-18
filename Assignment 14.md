

```python
1. What does RGBA stand for?
Answer:
RGBA value is a tuple of 4 integers, each ranging from 0 to 255.
The four integers correspond to the amount of red, green, blue, and alpha (transparency) in the color.

```


```python
2. From the Pillow module, how do you get the RGBA value of any images?
Answer:
from PIL import ImageColor
ImageColor.getcolor('red', 'RGBA')
ImageColor.getcolor('green', 'RGBA')

  (0, 128, 0, 255)
```


```python
3. What is a box tuple, and how does it work?
Answer:
box tuple is a tuple value of four integers: the left edge x-coordinate, 
the top edge y-coordinate, the width, and the height, respectively

```


```python
4. Use your image and load in notebook then, How can you find out the width and height of an Image object?
Answer:
from PIL import Image
sImg = Image.open('a.jpg')
w,h = sImg.size
w,h
```


```python
5. What method would you call to get Image object for a 100×100 image, excluding the lower-left quarter of it?
Answer:
imageObj.crop((0, 50, 50, 50))
```


```python
6. After making changes to an Image object, how could you save it as an image file?
Answer:
By Calling the imageObj.save('my_filename.png') method of the Image object.

```


```python
7. What module contains Pillow’s shape-drawing code?
Answer:
ImageDraw module contains code to draw on images
```


```python
8. Image objects do not have drawing methods. What kind of object does? How do you get this kind of object?
Answer:
ImageDraw objects have shape-drawing methods such as point(), line(), or rectangle(). 
They are returned by passing the Image object to the ImageDraw.Draw() function

```
