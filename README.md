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
~~~
Name: PRAKASH V
REG:212225230211
~~~

~~~
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Load Dataset
df = pd.read_csv("titanic_dataset.csv")

# Display Dataset
print(df)

# Dataset Information
print(df.info())

# Statistical Summary
print(df.describe())

# Data Types
print(df.dtypes)

# Value Counts
print(df.value_counts())

# Age Column Value Counts
print(df['Age'].value_counts())

# Set PassengerId as Index
df.set_index("PassengerId", inplace=True)

# Describe Dataset
print(df.describe())

# Shape of Dataset
print(df.shape)

# Number of Unique Values
print(df.nunique())

# Countplot for Survival
sns.countplot(data=df, x='Survived')
plt.show()

# Unique Values in Pclass
print(df.Pclass.unique())

# Rename Column
df.rename(columns={'Sex':'Gender'}, inplace=True)

# Display Dataset
print(df)

# Catplot
sns.catplot(
    x="Gender",
    col="Survived",
    kind="count",
    data=df,
    height=7,
    aspect=.7
)
plt.show()

# Boxplot
df.boxplot(column="Age", by="Survived")
plt.show()

# Scatterplot
sns.scatterplot(x=df["Age"], y=df["Fare"])
plt.show()

# Boxplot with Hue
fig, ax1 = plt.subplots(figsize=(8,5))

sns.boxplot(
    ax=ax1,
    x='Pclass',
    y='Age',
    hue='Gender',
    data=df
)

plt.show()

# Another Boxplot
sns.boxplot(
    x='Pclass',
    y='Age',
    hue='Gender',
    data=df
)

plt.show()

# Catplot with Pclass
sns.catplot(
    data=df,
    col="Survived",
    x="Gender",
    hue="Pclass",
    kind="count"
)

plt.show()

# Pairplot
sns.pairplot(data=df)

plt.show()

# Correlation Matrix
corr1 = df.select_dtypes(include=['number']).corr()

# Heatmap
sns.heatmap(corr1, annot=True)

plt.show()
~~~

<img width="1042" height="373" alt="image" src="https://github.com/user-attachments/assets/53d0b667-fe79-4e4e-85a2-1767f7466215" />

<img width="553" height="513" alt="image" src="https://github.com/user-attachments/assets/7e75f4be-9509-4fee-ae43-7e5b404a0398" />

<img width="926" height="399" alt="image" src="https://github.com/user-attachments/assets/5cc03734-0eb4-4813-aa16-44d373e994fa" />

<img width="297" height="365" alt="image" src="https://github.com/user-attachments/assets/af9ce430-becf-45d9-9b33-04a4c6166b3f" />

<img width="1043" height="456" alt="image" src="https://github.com/user-attachments/assets/2be33d72-afca-47d0-a92d-9c5589f68ddc" />

<img width="427" height="333" alt="image" src="https://github.com/user-attachments/assets/4b6f624f-93b3-4d7b-85b1-c04016afa147" />

<img width="825" height="388" alt="image" src="https://github.com/user-attachments/assets/96697a4a-ea98-4538-aaee-f9d74ecfb46c" />

<img width="144" height="47" alt="image" src="https://github.com/user-attachments/assets/46c4c552-5c96-4aa7-84f4-7fbfb40d6deb" />

<img width="259" height="367" alt="image" src="https://github.com/user-attachments/assets/1657f1d0-abfb-406e-9db5-23c5a268f037" />

<img width="1010" height="730" alt="image" src="https://github.com/user-attachments/assets/bb0aab58-556e-4970-88b5-9055728fd797" />

<img width="366" height="44" alt="image" src="https://github.com/user-attachments/assets/b48910c8-e21a-4231-8135-a94401e63647" />

<img width="1042" height="380" alt="image" src="https://github.com/user-attachments/assets/342a25b5-e0fe-449c-afc5-dff6609a4e6c" />

<img width="1043" height="739" alt="image" src="https://github.com/user-attachments/assets/3eb11dae-afd1-4f1e-8ae6-45ae1aa1b4e3" />

<img width="992" height="763" alt="image" src="https://github.com/user-attachments/assets/3e4372ba-f9ee-434e-8a58-df0a880829fe" />

<img width="973" height="721" alt="image" src="https://github.com/user-attachments/assets/9836ea7e-02e8-4602-9105-fb4cf75c969b" />

<img width="1039" height="619" alt="image" src="https://github.com/user-attachments/assets/b88b45ca-650e-4eb9-a5ae-da5ce3e13cdc" />

<img width="1046" height="496" alt="image" src="https://github.com/user-attachments/assets/fee2b287-a3fb-4e8b-b2af-4aedc4fe702b" />

<img width="836" height="837" alt="image" src="https://github.com/user-attachments/assets/947e12e4-5f3a-417d-93ff-b50c4d471727" />

<img width="865" height="736" alt="image" src="https://github.com/user-attachments/assets/5b9e0fc3-7958-44d7-9781-5ad86e78e3ae" />

# RESULT
Thus, To perform Exploratory Data Analysis on the given data set is implemented successfully.
