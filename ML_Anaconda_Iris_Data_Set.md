# Project Name: Anaconda Installation and Working with Iris Data

# Created By Jed 27/03/2023 @ 2:00AM 


## First Phase
1. Download and install Anaconda distribution from https://www.anaconda.com/products/distribution
2. Download these two files from the iris dataset: https://archive.ics.uci.edu/ml/machine-learning-databases/iris/
    - iris.data: contains the data
    - iris.name: contains the attributes for columns and etc
3. Create a directory (folder) for your project and copy iris.data into it.

## Second Phase
1. Open Anaconda Navigator
2. Click on the "Environments" tab on the left-hand side of the window and create a new environment
    - Tip: It is recommended to create a new environment for a new project to help with flexibility,
    reproducibility, and isolation from the base environment
3. Download all required packages for the project on the right-hand side of the window.  (pandas, numpy, seaborn, matplotlib)
4. Click on "Home" and install and launch "Jupyter Notebook"
    - It will open your default web browser with a page displaying the directory of your PC(localhost)
5. Locate the directory (folder) you created with the iris.data
6. Click on "New" on the menubar and click on "Python 3 (ipykernel)" to create a Python file

## Third Phase
### A new tab will open. The web page editor is separated into cells(which accepts codes for input)
### Import Libraries
```python
import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Load the iris dataset into a DataFrame and add column labels
df = pd.read_csv('iris.data')

# Click on run on the menubar to interpret and check for errors

# Add column labels to the DataFrame
df.columns = ['sepal_length', 'sepal_width', 'petal_length', 'petal_width', 'class']

# EDA(matplotlib and seaborn) with Scatterplot 
sns.scatterplot(x='petal_length', y='petal_width', hue='class', data=df)
plt.show()

# Click on run to generate graph output

#For more matplotlib and seaborn plots;
#Visit: https://www.analyticsvidhya.com/blog/2022/07/step-by-step-exploratory-data-analysis-eda-using-python/

# You can change comments to prefered

### Hope you found this helpful :)