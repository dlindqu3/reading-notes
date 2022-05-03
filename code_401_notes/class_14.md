# Code 401 Reading Notes 
### 14. Read: 14 - Data Visualization  

####  source: "matplotlib-tutorial" [link](https://github.com/rougier/matplotlib-tutorial)
- create a figure and axes 

```python 
import numpy as np
import matplotlib as plt 

X = np.linspace(-np.pi, np.pi, 256, endpoint=True)
C, S = np.cos(X), np.sin(X)

plt.figure(figsize=(10,6), dpi=80)
plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-")
plt.plot(X, S, color="red",  linewidth=2.5, linestyle="-")
```


####  source: "User guide and Tutorial" [link](https://seaborn.pydata.org/tutorial.html)

```python 
import seaborn as sns

penguins = sns.load_dataset("penguins")
sns.histplot(data=penguins, x="flipper_length_mm", hue="species", multiple="stack")

f, axs = plt.subplots(1, 2, figsize=(8, 4), gridspec_kw=dict(width_ratios=[4, 3]))
sns.scatterplot(data=penguins, x="flipper_length_mm", y="bill_length_mm", hue="species", ax=axs[0])
sns.histplot(data=penguins, x="species", hue="species", shrink=.8, alpha=.8, legend=False, ax=axs[1])
f.tight_layout()

sns.jointplot(data=penguins, x="flipper_length_mm", y="bill_length_mm", hue="species")

```

#### Things I want to know more about 
- other libraries besides matplotlib and seaborn 