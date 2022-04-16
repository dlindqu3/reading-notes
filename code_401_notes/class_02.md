# Code 401 Reading Notes 
### 02. Read: 2 -  Testing and Modules   

####  source: Ana Paul Gomes, "In Tests We Trust - TDD with Python" [link](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932)

- "unit tests" are specific bits of code that test the functionality of your app 
- "Test-Driven Development" (TDD) is a strategy that emphasizes writing tests before moving on to building your project 
- developers typically arrange tests into their own folder, with .py files for each test
- for example, if you have a module called login.py elsewhere, inside the tests folder, you might have test_login.py 
- one common library for tests is pytest 

## sample setup:

```python 
class DetectGender(obj): 
  def run(self, name): 
    result = requests.get('https://api.genderize.io/?name={}'.format(name)).json()
    return result['gender']

def test_should_return_female_when_name_is_female(): 
  detector = DetectGender()
  result = detector.run('Emily')
  assert result == 'female' 

def test_should_return_male_when_name_is_male(): 
  detector = DetectGender()
  result = detector.run('Jerry')
  assert result == 'male' 

```

#### source: "What does the if __name__ == "__main__": do?" [link](https://www.geeksforgeeks.org/what-does-the-if-__name__-__main__-do/)

- it's useful to know whether you are importing a module's functions vs using the original .py file for that module 
- a module is a file that contains python definitions and statements 
- the associated file name is typically module_name.py
- the "main" function is all of the code at the top block level 
- __name__ is a built-in variable that evaluates to the name of the currently selected module 
- when a file is being run directly, __name__ is automatically set to the string "name" 
-  when you run in terminal "python file_name.py": 
  - all of the code at block level 1 gets executed 
- if __name__ = "main" executes code only if the file was run directly, and was not an import 

#### source: "Recursion" [link](https://www.geeksforgeeks.org/recursion/)

- recursion is the process by which a function directly or indirectly calls itself 
- a function that does this is called a "recursive function" 
- the base case is where the recursion stops 
- a function has direct recursion if it calls itself 
- a function has indirect recursion if it calls ANOTHER function that then calls the original function 

#### Things I want to know more about 
- I still don't exactly understand recursion 