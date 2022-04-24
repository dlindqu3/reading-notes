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

#### source: Anamika Kalwan, "What is Risk Analysis in Software Testing and how to perform it?" [link](https://www.edureka.co/blog/risk-analysis-in-software-testing/)
  - "risk" is the probability of any unwanted event 
  - for software testing, risk analysis is the process of identifying risks in your application and prioritizing them to test 
  - a "test plan" can help identify risks and their potential affects, as well as potential solutions 
  - examples of possible risks- 
    - new hardware 
    - new tech 
    - a new automation tool 
    - the sequence of code 
    - availability of test resources 
  - focus resources on high-risk areas 
    - high-risk: effects would be non-tolerable; the company might face a loss 
    - medium: tolerable but not desirable; limited risk of financial loss
    - low: tolerable; no risk of financial loss
  - how to perform a risk analysis: 
    - search for risks
    - analyze the effects of each individual risk 
    - list measures for each risk identified 

#### source: Martin Fowler, "TestCoverage" [link](https://martinfowler.com/bliki/TestCoverage.html)
  - code coverage is also know as test coverage 
  - coverage analysis helps you determine which parts of the code aren't being tested 

#### source: "Big O Notation" [link](https://www.youtube.com/watch?v=v4cd1O4zkGw)
  - constant time beats linear time if the data is sufficiently big
  - this author doesn't cover space complexity 
  - drop constants, add various steps, keep track of changes in different variables, and drop non-dominant terms 

#### Things I want to know more about 
- Big O - do we need to keep track of varying Big O scores within a given data structure? Or just be familiar with the range of possibilities? 