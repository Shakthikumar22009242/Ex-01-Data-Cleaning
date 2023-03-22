# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
# 1.Data_set 

```python
import pandas as pd
df=pd.read_csv("data_set.csv")
print(df)
df.head(10)

df.info()

df.isnull()

df.isnull().sum()

df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()

df.isnull().sum()
```

# 2.Loan_data

```python
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)

df.info()

df.isnull()

df.isnull().sum()

df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Gender'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Gender'].mode()[0])
df.head()

df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].median())
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()

df.info()

df.isnull().sum()
```

# OUPUT

# 1.Data_set
# Data:
![](dataEX01%201-1.png) 

# Non null before:
![](dataEX01%201-2.png)

# Mode:
![](dataEX01%201-3.png)

# Mean:
![](dataEX01%201-4.png)

# Median: 
![](dataEX01%201-5.png)

# Non null after:
![](dataEX01%201-6.png)


# 2.Loan_data
# Data:
![](dataEX01%202-1.png)

# Non null before:
![](dataEX01%202-2.png)

# Mode:
![](dataEX01%202-3.png)

# Mean:
![](dataEX01%202-4.png)

# Median:
![](dataEX01%202-5.png)

# Non null after:
![](dataEX01%202-6.png)


# RESULT

Thus, the given datas were read , cleansed and the cleaned data is saved into the file.