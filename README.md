# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required packages.
2.Print the present data and placement data and salary data.
3.Using logistic regression find the predicted values of accuracy confusion matrices.
4.Display the results

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: BALASUBRAMANIAM L
RegisterNumber: 24901213

import pandas as pd
data=pd.read_csv(r"/Placement_Data.csv")
data.head()
data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)
data1.head()
data1.isnull().sum()
data1.duplicated().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1["gender"]=le.fit_transform(data1["gender"])
data1["ssc_b"]=le.fit_transform(data1["ssc_b"])
data1["hsc_b"]=le.fit_transform(data1["hsc_b"])
data1["hsc_s"]=le.fit_transform(data1["hsc_s"])
data1["degree_t"]=le.fit_transform(data1["degree_t"])
data1["workex"]=le.fit_transform(data1["workex"])
data1["specialisation"]=le.fit_transform(data1["specialisation"])
data1["status"]=le.fit_transform(data1["status"])
data1
x=data1.iloc[:,:-1]
x
y=data1["status"]
y
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.linear_model import LogisticRegression
lr=LogisticRegression(solver="liblinear")
lr.fit(x_train,y_train)
y_pred=lr.predict(x_test)
y_pred
from sklearn.metrics import accuracy_score
accuracy=accuracy_score(y_test,y_pred)
accuracy
from sklearn.metrics import confusion_matrix
confusion=confusion_matrix(y_test,y_pred)
confusion
from sklearn.metrics import classification_report
classification_report1=classification_report(y_test,y_pred)
print(classification_report1)
lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])

*/
```

## Output:
 ![ex5](https://github.com/user-attachments/assets/cf1c3592-acd2-4036-928d-c0c5d9fbbc84)
# Data
![image](https://github.com/user-attachments/assets/f89bc67e-76a1-48c7-8471-23e8b6ea4afa)
# XDATA
![image](https://github.com/user-attachments/assets/253a0aee-7a10-4249-b5a0-7e07d292c42a)
# Y STATUS
![image](https://github.com/user-attachments/assets/35cdb683-f77c-4596-889f-ff51281a16e7)
# Y PRED
![image](https://github.com/user-attachments/assets/cec741bc-f3bb-42a3-b691-c2e21837cece)
# confusion data
![image](https://github.com/user-attachments/assets/7f36ff77-655e-4622-bdbc-df5598e7c3e9)
# CLASSSIFICATION
![image](https://github.com/user-attachments/assets/c6040cff-9ee8-456c-9f8c-5c8ea82635de)

## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
