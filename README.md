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

# CODE:
```
import pandas as pd
df = pd.read_csv("SampleDS.csv")
df

df.shape

df.describe()

df.info()

df.isnull().sum()

df.dropna(how='any').shape

x = df.dropna(how='any')
x

df.dropna(how='all').shape
df

tot = df.dropna(subset=['TOTAL'],how='any')
tot

tot = df.dropna(subset=['M1','M2','M3','M4'],how='any')
tot

df.fillna(0)
df

df.fillna(method='ffill')

df.interpolate()

mn = df.TOTAL.mean()
mn

df.TOTAL.fillna(mn,inplace=False)

td = df.TOTAL.fillna(mn,inplace = True)

df

l = df.M1.interpolate()
l
df.isnull()

df.notnull()

df.dropna()

df.head()

df.tail()

df.info()

df.describe()
df

df.duplicated()
df

df.drop_duplicates(inplace=True)
df

df['cd']=pd.to_datetime(df['DOB'])
df

for x in df.index:
  if df.loc[x,'AVG']>100:
    df.drop(x,inplace = True)
df
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/a31b3013-be6d-49b9-8982-e4a4b244f376)

![image](https://github.com/user-attachments/assets/ee053209-9f5b-4e3e-b9a1-4b60752bba85)

![image](https://github.com/user-attachments/assets/e32d5974-8161-40db-8389-dbd825497113)

![image](https://github.com/user-attachments/assets/e4ea502f-c6ae-4a85-9789-cbdc858fa476)

![image](https://github.com/user-attachments/assets/b3091bcd-af24-40b4-9209-8f0a1946dadb)

![image](https://github.com/user-attachments/assets/1908a0d4-d9fb-4060-8247-14147b9431be)

![image](https://github.com/user-attachments/assets/dce69c3c-c4a8-47aa-b820-f3da6c6a3727)

![image](https://github.com/user-attachments/assets/aa75313a-32a6-42c3-a876-4ed1fc70dd33)

![image](https://github.com/user-attachments/assets/f18b01d9-a3d2-4a49-8a54-973bdef5ad43)

![image](https://github.com/user-attachments/assets/9e5fa19b-c48b-4777-a2a5-04aaf06e28a4)

![image](https://github.com/user-attachments/assets/4d63b9eb-1343-4093-a07d-0517efffe216)

![image](https://github.com/user-attachments/assets/bed8ed4f-326c-40ea-8937-5af73116f36a)

![image](https://github.com/user-attachments/assets/3d8205a5-50b1-4625-87bf-1e9dd8b95969)

![image](https://github.com/user-attachments/assets/3e9907a8-ed85-4974-9a24-16f2bf7c187c)

![image](https://github.com/user-attachments/assets/6fecf93c-04ce-4415-9075-5bbc6c9886ee)

![image](https://github.com/user-attachments/assets/5424ff9b-bbaa-4cbe-bf8a-df268a4a407c)

![image](https://github.com/user-attachments/assets/01cf5af9-00bf-4160-97df-2375db39306a)

![image](https://github.com/user-attachments/assets/6ec85ba0-3d1c-4cdd-ab08-f5a964d14a36)

![image](https://github.com/user-attachments/assets/0bd81410-7684-47ef-a060-5bb8e753d4c3)

![image](https://github.com/user-attachments/assets/e4228b03-71e8-41f3-9da5-f5195b1e9b1a)

![image](https://github.com/user-attachments/assets/38e41234-eac9-466c-9bd0-3389173bd962)

![image](https://github.com/user-attachments/assets/d819177e-1592-403b-b4d9-d60e48ac9922)

![image](https://github.com/user-attachments/assets/ef7d91c3-1ac1-4fec-8ba3-3dbd0aa97822)

![image](https://github.com/user-attachments/assets/86655b4c-34ca-4db7-8bdc-233c8b99fc76)

![image](https://github.com/user-attachments/assets/5614fb22-c4ad-40c8-8225-ece3405d160c)
