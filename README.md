# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
### Exploratory data analysis:
          import pandas as pd
          import numpy as np
          import matplotlib.pyplot as plt
          import seaborn as sns
          dt=pd.read_csv("/content/titanic_dataset.csv")
          dt
          
![image](https://github.com/Pandidharan/EXNO2DS/assets/118343569/0a395cca-fb18-43a3-8a3c-a2cebbb7bd62)

          dt.info()
          
![image](https://github.com/Pandidharan/EXNO2DS/assets/118343569/84c58eff-0ed0-4e6e-98bf-e3df414d3285)

          dt.shape
          
![image](https://github.com/Pandidharan/EXNO2DS/assets/118343569/fba476b9-f6b0-4547-a3fc-bf9ea28a9fd9)

          dt.set_index("PassengerId",inplace=True)
          dt.describe()
          
![image](https://github.com/Pandidharan/EXNO2DS/assets/118343569/e9c7ae20-cf61-43eb-ae8a-2247e313ba6a)


# RESULT
        <<INCLUDE YOUR RESULT HERE>>
