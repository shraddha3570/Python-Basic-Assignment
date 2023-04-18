

```python
1. In what modes should the PdfFileReader() and PdfFileWriter() File objects will be opened?
Answer:
Files will be opened in binary mode., read binary (rb) for PdfFileReader() and write binary (wb) PdfFileWriter()
```


```python
2. From a PdfFileReader object, how do you get a Page object for page 5?
Answer:
Calling getPage(4) will return a Page object for page 5 since page 0 is the first page

```


```python
3. What PdfFileReader variable stores the number of pages in the PDF document?
Answer:
The PdfFileReader.numPages variable stores an integer of the number of pages in the PdfFileReader object
```


```python
4. If a PdfFileReader object’s PDF is encrypted with the password swordfish, 
what must you do before you can obtain Page objects from it?
Answer:
Before we obtain the page object from it, the pdf has to be decrypted by calling .decrypt('swordfish')

```


```python
5. What methods do you use to rotate a page?
Answer:
The rotateClockwise() and rotateCounterClockwise() methods. The degrees to rotate is passed as an integer argument

```


```python
6. What is the difference between a Run object and a Paragraph object?
Answer:
Run Objects :
Runs are contiguous groups of characters within a paragraph with the same style
Paragraph Object :  A document contains multiple paragraphs. A paragraph begins on a new line and contains multiple 
runs.The Document object contains a list of Paragraph objects for the paragraphs in the document. 
```


```python
7. How do you obtain a list of Paragraph objects for a Document object that’s stored in a variable named doc?
Answer:
By using doc.paragraphs
#!pip install python-docx
import docx
doc = docx.Document('example.docx')
doc.paragraphs
```


```python
8. What type of object has bold, underline, italic, strike, and outline variables?
Answer:
A Run object has bold, underline,italic,strike and outline variables
```


```python
9. What is the difference between False, True, and None for the bold variable?
Answer:
False makes it always not bolded, no matter what the style’s bold setting is.
True always makes the Run object bolded
None will make the Run object just use the style’s bold setting.
```


```python
10. How do you create a Document object for a new Word document?
Answer:
By Calling the docx.Document() function.
```


```python
11. How do you add a paragraph with the text 'Hello, there!' to a Document object stored in a variable named doc?
Answer:
import docx
doc = docx.Document()
doc.add_paragraph('Hello there!')
doc.save('hellothere.docx')
```


```python
12. What integers represent the levels of headings available in Word documents?
Answer:
Integer from 0 to 4
The integer 0 makes the heading the Title style, which is used for the top of the document.
Integers 1 to 4 are for various heading levels, with 1 being the main heading and 4 the lowest subheading

```
