# EX-05-Feature-Generation

# AIM

To read the given data and perform Feature Generation process and save the data to a file.

# Explanation

Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

# ALGORITHM

## STEP 1

Read the given Data

## STEP 2

Clean the Data Set using Data Cleaning Process

## STEP 3

Apply Feature Generation techniques to all the feature of the data set

## STEP 4

Save the data to the file

# CODE

data.csv
import pandas as pd   
import seaborn as sbn 
df=pd.read_csv("/content/data.csv") 
df.info() 
df.isnull().sum()
from sklearn.preprocessing import LabelEncoder 
le = LabelEncoder() 
df['Ord_2'] = le.fit_transform(df['Ord_2']) 
sbn.set(style ="darkgrid") 
sbn.countplot(df['Ord_2'])
from sklearn.preprocessing import OneHotEncoder 
enc = OneHotEncoder() 
enc = enc.fit_transform(df[['City']]).toarray() 
encoded_colm = pd.DataFrame(enc) 
df = pd.concat([df, encoded_colm], axis=1) 
df = df.drop(['City'], axis=1) 
df.head(10) 
df = pd.get_dummies(df, prefix=['Ord_2'], columns=['Ord_2']) 
df.head(10) 
df = pd.get_dummies(df, prefix=['Ord_1'], columns=['Ord_1']) 
df.head(10)

# encoding.csv

import pandas as pd 
import seaborn as sbn 
data=pd.read_csv("/content/Encoding Data.csv") 
data.info() 
data.isnull().sum() from sklearn.preprocessing import LabelEncoder 
le = LabelEncoder() data['ord_2'] = le.fit_transform(data['ord_2']) 
sbn.set(style ="darkgrid") 
sbn.countplot(data['ord_2']) from sklearn.preprocessing import OneHotEncoder 
en = OneHotEncoder() 
en = en.fit_transform(data[['nom_0']]).toarray() 
encoded_colm = pd.DataFrame(en) 
data= pd.concat([data, encoded_colm], axis=1) 
data= data.drop(['nom_0'], axis=1) 
data.head(10) 
data = pd.get_dummies(df, prefix=['bin_2'], columns=['bin_2']) 
data.head(10)

# titanic.csv

import pandas as pd 
import seaborn as sbn 
dt=pd.read_csv("/content/titanic_dataset.csv") 
dt.info() 
dt.isnull().sum() 
dt['Age']=dt['Age'] . fillna(dt ['Age'].mean()) 
dt ['Cabin']=dt['Cabin']. fillna(dt['Cabin']. mode() [0]) 
dt ['Embarked']=dt['Embarked'] . fillna(df ['Embarked'].mode( )[0]) 
dt.isnull().sum( ) from sklearn.preprocessing import LabelEncoder 
lc = LabelEncoder() 
df['Sex'] = lc.fit_transform(df['Sex']) 
sbn.set(style ="darkgrid") 
sbn.countplot(df['Sex']) from sklearn.preprocessing import OneHotEncoder 
enc= OneHotEncoder() 
enc= enc.fit_transform(dt[['Name']]).toarray() 
encoded_colm = pd.DataFrame(enc) 
dt= pd.concat([dt, encoded_colm], axis=1) 
dt= dt.drop(['Name'], axis=1) 
dt.head(10) 
dt = pd.get_dummies(dt, prefix=['Ticket'] ,columns=['Ticket']) 
df.head(10) 
dt = pd.get_dummies(dt, prefix=['Embarked'] ,columns=['Embarked']) 
df.head(10)

# OUPUT

# Data.csv

![image](https://user-images.githubusercontent.com/129577149/232750015-e16afed1-a837-409d-ad24-9a42b2898cf8.png)


![image](https://user-images.githubusercontent.com/129577149/232750147-b3c55f1e-1552-44eb-ba2e-0903ad242341.png)


![image](https://user-images.githubusercontent.com/129577149/232750337-a7e6a737-b092-46da-a5b5-f235dab0ec45.png)


![image](https://user-images.githubusercontent.com/129577149/232750411-5be5bfb3-0d33-4d54-b9c2-3479c903a379.png)


![image](https://user-images.githubusercontent.com/129577149/232750536-f02a7d99-b263-4b40-a084-36a31011d011.png)

# Encoding.csv

![image](https://user-images.githubusercontent.com/129577149/232750763-3057c579-009b-42ee-895e-866163172364.png)

![image](https://user-images.githubusercontent.com/129577149/232750953-be02c988-5687-4497-9d4e-4bde7ad28689.png)

![image](https://user-images.githubusercontent.com/129577149/232751008-9cccbcea-fcbb-4f22-8739-92e38d05d71e.png)

![image](https://user-images.githubusercontent.com/129577149/232751099-f7a8254e-5a92-4a9d-9467-1bf7b27b880c.png)

# Titanic.csv

![image](https://user-images.githubusercontent.com/129577149/232751233-8040fc77-636c-4e1f-9b23-a7b20ef4cfd5.png)


![image](https://user-images.githubusercontent.com/129577149/232751287-3a01a78a-38d8-4f7d-9770-6b9ef3dc6331.png)


![image](https://user-images.githubusercontent.com/129577149/232751355-3b105309-88b8-4c6b-bf5f-f28ee08ce7a0.png)


![image](https://user-images.githubusercontent.com/129577149/232751412-f9ef668e-7418-4221-84cd-716208732f61.png)


![image](https://user-images.githubusercontent.com/129577149/232751528-23bb70b9-3da8-4cb4-bccc-1f3e6ea74636.png)


![image](https://user-images.githubusercontent.com/129577149/232751601-99b27ae9-1304-4488-b88e-04a0139038ed.png)

# RESULT:

Thus the program for Feature Generation is executed successfully.




