# Code 401 Reading Notes 
### 13. Read: 13 - Linear Regressions  

####  source: Manu Jeevan, "How to run Linear regression in Python scikit-Learn" [link](https://bigdata-madesimple.com/how-to-run-linear-regression-in-python-scikit-learn/)
- imports/setup: 

```python
%matplotlib inline 

import numpy as np 
import pandas as pd 
import scipy.stats as stats 
import matplotlib.pyplot as plt 
import sklearn 

#convert to df 
bos = pd.DataFrame(boston.data)
bos.columns = boston.featur_names 

#make a new col 
bos['Price'] = boston.target

#least squares setup 
from sklear.linear_model import LinearRegression
X = bos.drop('Price', axis = 1)

#create regression obj 
lm = LinearRegression()

lm.fit(X, bos.Price)

lm.coef_

#calculate MSE

#split data, train-test 

#run a residual to see if data falls around 0, as expected 
```

####  source: "Introduction to Simple Linear Regression" [link](https://www.youtube.com/watch?v=KsVBBJRb9TE)
- plot a line of best fit 
- account for varying y values around expected line with a random error component

#### Things I want to know more about 
- where does a data analyst's job end and an software engineer's job begin?