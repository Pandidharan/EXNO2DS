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

### Categorical data analysis:
```
dt.nunique()
```
![311099897-24404bf7-7cbe-4dfe-934e-4df366660737](https://github.com/Kowsalyasathya/EXNO2DS/assets/118671457/f2d58808-a860-401a-987b-990f2da4da29)
```
dt["Survived"].value_counts()
```
![311099933-018abaad-a788-4cf6-b2ae-a2ab28772793](https://github.com/Kowsalyasathya/EXNO2DS/assets/118671457/d2b11229-b562-4a0a-8e19-afe5fe4cb049)

```
per=(dt["Survived"].value_counts()/dt.shape[0]*100).round(2)
per
```
![311099956-44a97d7b-081e-470b-b88a-130d20867e4d](https://github.com/Kowsalyasathya/EXNO2DS/assets/118671457/58634f63-04af-45f3-8ddf-f1b3539edd03)

### Univariate analysis:
```
sns.countplot(data=dt,x="Survived")
```
![311099986-6923fca1-1bb8-426b-8913-bf5efc5f8870](https://github.com/Kowsalyasathya/EXNO2DS/assets/118671457/cb6ca763-ab0d-46f1-a73a-bf31c2e8f68c)

```
dt.Pclass.unique()
```
![311100655-d506691d-69cd-4ec5-be17-d1e34caa37cc](https://github.com/Kowsalyasathya/EXNO2DS/assets/118671457/e09d9f9f-67ef-40cc-893a-21ae612bed91)

```
dt.rename(columns = {'Sex':'Gender'},inplace=True)
dt
```
![311100681-af221019-adaa-4f5f-85a6-3f4b13d0cb33](https://github.com/Kowsalyasathya/EXNO2DS/assets/118671457/a4565b9c-fab8-4843-b870-38686e37157e)

### Bivariate analysis:
```
sns.catplot(x="Gender",col="Survived",kind="count",data=dt,height=5,aspect=.7)
```
![311100726-59a84a4b-8b93-4896-9a7d-0b5046695f72](https://github.com/Kowsalyasathya/EXNO2DS/assets/118671457/4707cc33-49b4-4767-bd2d-f160418e5b9f)

```
sns.catplot(x='Survived',hue="Gender",data=dt,kind="count")
```
![311100762-cac9226f-2cb4-4693-99ab-aa262cd28e3a](https://github.com/Kowsalyasathya/EXNO2DS/assets/118671457/f3352ce5-516a-4431-b7ae-51e90caee787)

```
dt.boxplot(column="Age",by="Survived")
```
![311100774-17ab0861-c128-47e7-a313-116bedd8e100](https://github.com/Kowsalyasathya/EXNO2DS/assets/118671457/8212e3d7-3564-4b73-909f-010654945a16)

```
sns.scatterplot(x=dt["Age"],y=dt["Fare"])
```
![311100789-359b469f-9633-44f0-aa1b-d7474f573f2a](https://github.com/Kowsalyasathya/EXNO2DS/assets/118671457/0e3d0459-6891-41ab-b7f1-2d1f86286aca)

```
sns.jointplot(x="Age",y="Fare",data=dt)
```
![311100804-290d6166-e4f3-471b-8582-72600004084f](https://github.com/Kowsalyasathya/EXNO2DS/assets/118671457/6ca0ee23-5f26-45b1-8923-a4f693b025d2)

### Multivariate analysis:
```
fig,ax1=plt.subplots(figsize=(8,5))
pt=sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Gender',data=dt)
```
![311100829-cfad821e-1d27-4c6d-96da-a43c261076c6](https://github.com/Kowsalyasathya/EXNO2DS/assets/118671457/6de78ee3-38f4-4169-a6e2-fa05b8404891)
```
sns.catplot(data=dt,col="Survived",x="Gender",hue="Pclass",kind="count")
```
![311100863-633922ee-abf2-400f-bd54-1e6d0533467e](https://github.com/Kowsalyasathya/EXNO2DS/assets/118671457/41251fb2-4f65-4796-ac6c-0f1a442ccab1)

# RESULT
Thus the Exploratory Data Analysis process is performed successfully on the given data using python code.
