# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE and OUTPUT
```
import pandas as pd
df= pd.read_csv("Data_set.csv")
print (df)
```
![screenshort(1)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/889a730e-abfa-4505-a8d3-9e353954d00d)
```
df.head(10)
```
![screenshort(2)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/43cbeb62-c8dc-4020-bd47-d0ddedfe96ae)
```
df.info()
```
![screenshort(3)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/a3879534-192d-4bbb-b731-ebe765690775)
```
df.isnull()
```
![screenshort(4)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/8fcf6b78-a2b2-4ed0-ac6e-37fdd5e1114a)
```
df.isnull().sum()
```
![screenshort(5)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/aff3cca0-9013-4bcb-b97e-72b03be1a9f4)
```
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df.head()
```
![screenshort(6)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/1751629a-39e7-411f-b87f-0b3a894eb9b5)
```
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df.head()
```
![screenshort(7)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/b0762ff0-ff23-43db-a9a8-15ff6e6bb201)
```
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
```
![screenshort(8)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/a9bd37e2-5d52-4db8-b800-5a65a6e6bd02)
```
df['rating']=df['rating'].fillna(df['rating'].mean())
df.head()
```
![screenshort(9)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/2bb860a8-9639-4a3e-b297-6c728359e72b)
```
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
```
![screenshort(10)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/9c4910a4-3f74-4de7-9f93-af9ddac0b8a8)
```
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
```
![screenshort(11)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/d671a5a5-0ca2-4fa4-9bdc-a3bc150fe5b5)
```
import pandas as pd
df= pd.read_csv("Loan_data.csv")
print(df)
```
![screenshort(12)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/b7a99602-ae1f-40c4-b84e-71831302984b)
```
df.head()
```
![screenshort(13)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/978ea362-2fa4-41d2-9439-a30154a5287c)
```
df.info()
```
![screenshort(14)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/d0e4864f-c95f-4b76-90d1-6f162c16701b)
```
df.isnull()
```
![screenshort(15)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/81d928ca-c076-4c12-819b-9ba2f654d108)
```
df.isnull().sum()
```
![screenshort(16)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/f0467f6e-91c3-4cd1-93ad-fc9be617462f)
```
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df.head()
```
![screenshort(17)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/44545c15-5ff8-49a6-bb58-d476b12be488)
```
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df.head()
```
![screenshort(18)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/56c91cd8-8939-4178-b27b-a0ce3f74b4cd)
```
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df.head()
```
![screenshort(19)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/3e671d4b-245b-46e2-a474-0d4dfaacdc4a)
```
df['Self_Employed']=df['Self_Employed'].fillna(df['Dependents'].mode()[0])
df.head()
```
![screenshort(20)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/67b23255-8888-4a68-b5b9-60e664920562)
```
df['Gender']=df['Gender'].fillna(df['Dependents'].mode()[0])
df.head()
```
![screenshort(21)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/3f3e1b53-e1bd-4dda-ab54-383d9493c6e6)
```
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
```
![screenshort(22)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/0a0d4427-062f-4fc9-8fd8-cfd60ced91a1)
```
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df.head()
```
![screenshort(23)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/d02e4408-cd79-4df0-8ed8-c38f1380aa18)
```
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
```
![2023-08-26 (24)](https://github.com/Sathya-006/ODD2023-Datascience-Ex01/assets/121661327/1f9796c6-a1f9-4c13-aa7b-fa729dd8b927)

# RESULT
Thus the given data was read and data cleaning was performed and saved  
