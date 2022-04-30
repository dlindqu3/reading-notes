# Code 401 Reading Notes 
### 12. Read: 12 - Pandas

####  source: "10 minutes to pandas" [link](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)
  
```python 
import numpy as np 
import pandas as pd 

s = pd.Series([1,2,3,np.nan,5,6])

df = pd.read_csv('my_file.csv')

df.dtypes 

df.head()

df.describe()

df.loc['blueberries'] #displays a row of data with index=blueberries

df.iloc[0:99] #displays the first 100 rows 

df[df["profit"] > 200] #displays rows with profit over 200 

```

- you can also merge, concat, and group data from dataframes


#### Things I want to know more about 
- ways to import data if you get errors 