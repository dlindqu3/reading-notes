# Code 401 Reading Notes 
### 04. Read: 04 -  Topic 

####  source: "Classes and Objects" [link](https://www.learnpython.org/en/Classes_and_Objects)
  - classes are like a template to create objects

  ```python 
  class Dog(): 

    def __init__(self, breed): 
      this.breed = breed 
    def speak (self): 
      print('bark bark')
  
  Sammy = Dog('lab')
  Sammy.speak()
  Sammy.breed
  ```

#### source: Abhirag Awasthi, "Thinking Recursively in Python" [link](https://realpython.com/python-thinking-recursively/)
  - each recursive call has its own execution context 
  - to maintain state, you need to either pass state through each recursive call OR  
  - keep a global state 
  - a recursive data structure can be defined in terms of smaller versions of itself (like a list, set, tree, dictionary, etc.)

#### source: Reuven M. Lerner, "Testing with pytest: Fixtures and Coverage" [link](https://www.linuxjournal.com/content/python-testing-pytest-fixtures-and-coverage)
  - fixtures are objects available to all tests
  - set a fixture by putting "@pytest.fixture" above a function 
  - use it in a test by putting it in a test's parameter list 
  - code coverage checks whether or not all of the tests have rull all of the code 
  - to use, perhaps need to import pytest-cov 

#### Things I want to know more about 
- in python, what other structures besides set, list, tree, and dictionary are recursive? 
