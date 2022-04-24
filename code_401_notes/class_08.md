# Code 401 Reading Notes 
### 08. Read: 08 -  Ten Thousand 3

####  source: Josh Petty, "List Comprehensions in Python" [link](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)
  
  ```python 
  #creating lists with list comprehension 
  multiples_of_three = [ x*3 for x in range(10) ]
  even_nums = [ x for x in range(1,20) if x % 2 == 0]

  #reading lines of a file with list comprehension
  file = open("dreams.txt", 'r')
  poem = [ line for line in file ]

  for line in poem:
    print(line)

#functions used within list comprehension
  def double(x):
    return x*2

  nums = [double(x) for x in range(1,10)]
  print(nums)
  ```

#### Things I want to know more about 
- other applications of list comprehension 