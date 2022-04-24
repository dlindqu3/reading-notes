# Code 401 Reading Notes 
### 06. Read: 06 -  Ten Thousand Game 1

####  source: "How to use Random Module in Python" [link](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)
  ```python 
  import random 
  print random.randint(0,7)

  print random.random * 100

  teams = ['chelsea', 'tottenham', 'liverpool']
  print random.choice(teams)

  random.shuffle(teams)
  print(teams)

  print random.randrange(0,20,3)
  ```

#### source: Martin Fowler, "TestCoverage" [link](https://martinfowler.com/bliki/TestCoverage.html)
  - code coverage is also know as test coverage 
  - coverage analysis helps you determine which parts of the code aren't being tested 

#### source: "Big O Notation" [link](https://www.youtube.com/watch?v=v4cd1O4zkGw)
  - constant time beats linear time if the data is sufficiently big
  - this author doesn't cover space complexity 
  - drop constants, add various steps, keep track of changes in different variables, and drop non-dominant terms 

#### Things I want to know more about 
- Big O - do we need to keep track of varying Big O scores within a given data structure? Or just be familiar with the range of possibilities? 