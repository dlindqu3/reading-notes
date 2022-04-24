# Code 401 Reading Notes 
### 07. Read: 07 -  Ten Thousand 2

####  source: Leodanis Pozo Ramos, "Python Scope & the LEGB Rule: Resolving Names in Your Code" [link](https://realpython.com/python-scope-legb-rule/)
  - global: 
    - global scope is the same as __main__ in a given file 
    - to find global variables: run -- dir()
    - to assign a global var from within a function: prefix var name with "global" 
    - globals() called in the .py file will list global vars from the current module 
  - nonlocal: 
    - these can be accessed from inner functions, but not assigned or updated 

#### source: "Don't be CONFUSED by BIG O notation anymore!" [link](https://www.youtube.com/watch?v=5Uqawfl0VHQ)
  - common Big O scores: 
    - O(1), O(logN), O(N), O(NlogN), O(N^k)
    - logarithmic complexity is typically efficient
    - binary search has logarithmic time complexity 

#### Things I want to know more about 
- Big O - do we need to keep track of varying Big O scores within a given data structure? Or just be familiar with the range of possibilities? 