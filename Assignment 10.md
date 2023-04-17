

```python
1. How do you distinguish between shutil.copy() and shutil.copytree()?
Answer: shutil.copy : Copies a single file    
        shutil.copytree() : will copy an entire folder and every folder and file contained in it
```


```python
2. What function is used to rename files??
Answer: 
import os
os.rename("a.txt","anew.txt")
```


```python
3. What is the difference between the delete functions in the send2trash and shutil modules?
Answer:
Using send2trash, we can send files to the Trash or Recycle Bin instead of permanently deleting them.
The shutil module’s rmtree() function can be used to delete files or folders. But, this function delete the files permanently.
The operations cannot be undone if there were any accidental deletions performed.

```


```python
4.ZipFile objects have a close() method just like File objects’ close() method.
What ZipFile method is equivalent to File objects’ open() method?
Answer: 
The zipfile.ZipFile() function is equivalent to the open() function; 
the first argument is the filename, and the second argument is the mode to open the ZIP file in (read, write, or append).

```


```python
5. Create a programme that searches a folder tree for files with a certain file extension (such as .pdf or .jpg). 
Copy these files from whatever location they are in to a new folder.

Answer:

def selectiveCopy(source, extensions, destFolder):
    folder = os.path.abspath(source)
    destFolder = os.path.abspath(destFolder)
    print('Looking in', source, 'for files with extensions of', ', '.join(extensions))
    for foldername, subfolders, filenames in os.walk(source):
        for filename in filenames:
            name, extension = os.path.splitext(filename)
            if extension in extensions:
                fileAbsPath = foldername + os.path.sep + filename
                print('Coping', fileAbsPath, 'to', destFolder)
                shutil.copy(fileAbsPath, destFolder)

extensions = ['.pdf','.jpg']
source = "C:\\Users\\shraddha\\Desktop\\source"
destFolder = "C:\\Users\\shraddha\\Desktop\\destination"
selectiveCopy(source, extensions, destFolder)

    Looking in C:\Users\shraddha\Desktop\source for files with extensions of .pdf, .jpg
    Coping C:\Users\shraddha\Desktop\source\a.pdf to C:\Users\shraddha\Desktop\destination
    Coping C:\Users\shraddha\Desktop\source\s.jpg to C:\Users\shraddha\Desktop\destination
```
