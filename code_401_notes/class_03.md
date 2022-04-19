# Code 401 Reading Notes 
### 03. Read: 03 -  FileIO & Exceptions    

####  source: James Mertz, "Reading and Writing Files in Python (Guide)" [link](https://realpython.com/read-write-files-python/)

- a "file" is a contiguous set of bits that stores data 
- files are typically composed of a header, data, and end of file "EOF" 
- a file path is composed of a folder path, file name, and extension 
- files typically denote a line ending with \r, \n, or \r\n
- the two most common character encodings are ASCII and Unicode 
- ASCII is a subset of Unicode 

```python 
new_file = open('results.txt')

try: 
  #further file processing 
finally: 
  new_file.close()
```

- author suggests an alternative, the "with" statement, which automatically closes the file once it exits the with block, even in case of error 
- 'r' opens in read mode 

```python 
with open('results.txt', 'r') as my_file: 
  #further processing 
```

- 3 categories of file objects: 
  - text files 
  - buffered binary files 
  - raw binary files 

- common methods: 
  - .read()
  - .write(string)


#### source: Said van de Klundert, "Python Exceptions: An Introduction" [link](https://realpython.com/python-exceptions/)

- in python, errors can be syntax errors or exceptions 
- exceptions occur when the syntax of the code is correct but an error occurs
- we can use "raise" to produce an exception if something occurs 
- assertion error: if some condition is true, program continues; if false, throw an assertion error exception 
- example of assertion: 

```python 
import sys
assert ('linux' in sys.platform), "This code only works on linux."

#if run on a mac: 
Traceback (most recent call last):
  File "<input>", line 2, in <module>
AssertionError: This code only works on linux.
```
 
 - try/except example: 

 ```python 
try:
    linux_interaction()
except:
    print('Linux_interaction function was not executed')
 ```

 - other option: 

 ```python 
try:
    linux_interaction()
except AssertionError as error:
    print(error)
    print('linux_interaction function was not executed')
 ```

#### Things I want to know more about 
- opening other types of files, like .csv 