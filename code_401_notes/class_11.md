# Code 401 Reading Notes 
### 11. Read: 11 - Data Analysis

####  source: "Overview" [link](https://jupyterlab.readthedocs.io/en/stable/getting_started/overview.html)
  - Jupyter lab allows you to work with data in a kernel-backed environment 
  - you can also run files using terminal commands 
  - when a notebook is open, you are in "command" mode 
  -within a notebook, you can write in markdown format
  - coding in a cell produces output under that cell

#### source: "NumPy Tutorial: Data Analysis with Python" [link](https://www.dataquest.io/blog/numpy-tutorial-python/)
  - to render csv data, you can create a list of numpy lists 

```python 
import csv
with open('winequality-red.csv', 'r') as f:
    wines = list(csv.reader(f, delimiter=';'))

#print first 3 rows: 
print(wines[:3])

import numpy as np
wines = np.array(wines[1:], dtype=np.float)
wines.shape

wines[:,11] * 2

wines[:,11].sum()

```

#### Things I want to know more about 
- Setting up Jupyter 