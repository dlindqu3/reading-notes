# Code 401 Reading Notes 
### 19. Automation   

####  source: Sejal Jaiswal, "Python Regular Expression Tutorial" [link](https://www.datacamp.com/tutorial/python-regular-expression-tutorial)

```python 
import re

pattern = r"Cookie"
sequence = "Cookie"
if re.match(pattern, sequence):
    print("Match!")
else: print("Not a match!")

# "." matches any char except new line: 
re.search(r'Co.k.e', 'Cookie').group()
'Cookie'

#"^" matches the start of a string
#"$" matches end of string 
#[a-zA-Z0-9] 
# If the first character of the set is ^, all the characters that are not in the set will be matched

re.search(r'Co+kie', 'Cooookie').group()
'Cooookie'
```

####  source: "shutil — High-level File Operations" [link](https://pymotw.com/3/shutil/)
- helps with copying and archiving files

```python 
import glob
import shutil

print('BEFORE:', glob.glob('shutil_copyfile.*'))

shutil.copyfile('shutil_copyfile.py', 'shutil_copyfile.py.copy')

print('AFTER:', glob.glob('shutil_copyfile.*'))


#command line: python3 shutil_copyfile.py
#BEFORE: ['shutil_copyfile.py']
#AFTER: ['shutil_copyfile.py', 'shutil_copyfile.py.copy']


```


####  source: "Super quick Python automation ideas" [link](https://www.youtube.com/watch?v=qbW6FRbaSl0)
1. automatically move files and rename them 
2. calculating compound interest 


#### Things I want to know more about 
-  other commonly automated tasks in web dev 