# Code 401 Reading Notes 
### 42. Pythonisms

####  source: Bob Belderbos, "Enriching Your Python Classes With Dunder (Magic, Special) Methods" [link](https://dbader.org/blog/python-dunder-methods)
- dunder methods let you imitate the behaviour of built-in types 
- common dunder methods: init, str, repr
- make an object callable with the __call__

####  source: Dan Bader, "Python Iterators: A Step-By-Step Introduction" [link](https://dbader.org/blog/python-iterators)
- under the hood, iterable objects might support the __iter__ and __next__ methods 


####  source: Dan Bader, "What Are Python Generators?" [link]()
- a generator can help you write iterators quickly with the "yield" command 
- they abstract away and replace much of the extra syntax of an iterator 

#### Things I want to know more about 
- other common dunder methods 