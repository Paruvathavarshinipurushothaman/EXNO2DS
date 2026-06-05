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
 ```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv('titanic_dataset.csv')
df
df.info()
df.shape
df.set_index('PassengerId',inplace=True)
df.describe()
df.shape
df.nunique()
df["Survived"].value_counts()
per=(df["Survived"].value_counts()/df.shape[0]*100).round(2)
per
import seaborn as sns
sns.countplot(data=df,x='Survived')
df
df.Pclass.unique()
df.rename(columns={'Sex':'Gender'},inplace=True)
df
sns.catplot(x="Gender",col="Survived",kind="count",data=df,height=5,aspect=.7)
df.boxplot(column="Age",by="Survived")
sns.scatterplot(x=df["Age"],y=df["Fare"])
sns.jointplot(x="Age",y="Fare",data=df)
import matplotlib.pyplot as plt
fig,ax1=plt.subplots(figsize=(8,5))
plt=sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Gender',data=df)
sns.catplot(data=df,col="Survived",x="Gender",hue="Pclass",kind="count")
import numpy as np
#Select only numeric columns before calculating correlation 
numeric_df=df.select_dtypes(include=np.number)

#Calculate correlation for numeric columns only
corr=numeric_df.corr()

#Generate the heatmap
sns.heatmap(corr, annot=True)
sns.pairplot(df)
```

<img width="1063" height="352" alt="image" src="https://github.com/user-attachments/assets/7a5e9842-11d5-48da-98d2-e5f1a20c99d2" />
<img width="545" height="512" alt="image" src="https://github.com/user-attachments/assets/d8296659-1469-4e95-854c-3400ad0363f6" />
<img width="162" height="56" alt="image" src="https://github.com/user-attachments/assets/e057beac-b911-4841-8993-7658075f760e" />
<img width="813" height="386" alt="image" src="https://github.com/user-attachments/assets/9b8a4e5a-9df3-41eb-a425-a700f8ab7dfc" />
<img width="150" height="52" alt="image" src="https://github.com/user-attachments/assets/51b0d8e3-f731-43a7-b0c6-3e50d588b9c1" />
<img width="252" height="337" alt="image" src="https://github.com/user-attachments/assets/9dd9c6a7-0af8-4f4f-b1d3-509922c66f25" />
<img width="381" height="113" alt="image" src="https://github.com/user-attachments/assets/7fe0a0ca-4204-4281-ba7c-fecfcf437472" />
<img width="397" height="111" alt="image" src="https://github.com/user-attachments/assets/29707fb2-9be1-4806-99b2-b5e7181601dc" />
<img width="991" height="733" alt="image" src="https://github.com/user-attachments/assets/0b68a2a3-2bf6-42a5-995b-b93172d737b5" />
<img width="1057" height="422" alt="image" src="https://github.com/user-attachments/assets/c4c40558-565c-4402-ab7c-af09db9aa6e4" />
<img width="387" height="46" alt="image" src="https://github.com/user-attachments/assets/e18b9d1c-94e4-4848-96b6-b0633779593e" />
<img width="1070" height="416" alt="image" src="https://github.com/user-attachments/assets/c580562b-c47a-4a31-be60-dbf1344582d2" />
<img width="1001" height="738" alt="image" src="https://github.com/user-attachments/assets/c3b9cb88-906d-48ea-9084-41b183bdaa93" />
<img width="960" height="777" alt="image" src="https://github.com/user-attachments/assets/acd019ca-f0e3-4eb3-91d7-485ee75f690d" />
<img width="960" height="741" alt="image" src="https://github.com/user-attachments/assets/f00011e4-d4d3-4985-af68-17127b00dc93" />
<img width="931" height="820" alt="image" src="https://github.com/user-attachments/assets/dfde569f-eb34-4bef-b479-90554b1e5e9b" />
<img width="953" height="603" alt="image" src="https://github.com/user-attachments/assets/eb248292-16f2-4d05-ab6d-707cf77bcec6" />
<img width="953" height="493" alt="image" src="https://github.com/user-attachments/assets/2df2ffb5-c741-4a46-a32a-39280f1525a8" />
<img width="852" height="727" alt="image" src="https://github.com/user-attachments/assets/fcc8f3d3-1eb4-4a2a-8705-e86e83587b8d" />
<img width="971" height="488" alt="image" src="https://github.com/user-attachments/assets/94999732-5cc7-414f-93c9-04c407928ab4" />
<img width="947" height="492" alt="image" src="https://github.com/user-attachments/assets/34b536c3-cfef-4ed4-8644-b92dd5ae9ca9" />


# RESULT
   Thus exploratory data analysis on the given data set is executed successfully.
