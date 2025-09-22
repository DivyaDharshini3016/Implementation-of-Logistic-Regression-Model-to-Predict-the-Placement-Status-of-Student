# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required packages and print the present data.

2.Print the placement data and salary data.

3.Find the null and duplicate values.

4.Using logistic regression find the predicted values of accuracy , confusion matrices.

5.Display the results.

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: Divya Dharshini S
RegisterNumber: 212224240039

import pandas as pd
data=pd.read_csv("Placement_Data.csv")
data.head()
data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)
data1.head()
data1.isnull()
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
from sklearn.metrics import classification_report
classification_report1=classification_report(y_test,y_pred)
print(classification_report1)
lr.predict([[1,80,1,90,1,1,90,1,0,85,1,85]])

*/
```

## Output:
<img width="909" height="198" alt="Screenshot 2025-09-22 110545" src="https://github.com/user-attachments/assets/5af4ec0f-222b-421b-ab41-420485b7d443" />

<img width="817" height="397" alt="Screenshot 2025-09-22 110614" src="https://github.com/user-attachments/assets/42a97f4b-fed9-4b71-b4b8-fb263750a62f" />

<img width="815" height="404" alt="Screenshot 2025-09-22 110703" src="https://github.com/user-attachments/assets/6dda0522-37f1-4d88-838a-c1768ab2e7f7" />

<img width="765" height="410" alt="Screenshot 2025-09-22 110726" src="https://github.com/user-attachments/assets/9934831a-c77b-426a-a917-50c9b708f4b6" />

<img width="400" height="210" alt="Screenshot 2025-09-22 110756" src="https://github.com/user-attachments/assets/b39dad3a-1ea7-4b1f-82c0-2180cc504fd7" />

<img width="558" height="50" alt="Screenshot 2025-09-22 110845" src="https://github.com/user-attachments/assets/1999f534-dfef-4636-8036-7832ce4307d5" />

<img width="464" height="148" alt="Screenshot 2025-09-22 110914" src="https://github.com/user-attachments/assets/02f066fd-5b0d-4259-af35-3dd0100bb519" />

<img width="110" height="30" alt="Screenshot 2025-09-22 110919" src="https://github.com/user-attachments/assets/e1fb7083-6c96-4e8c-ad96-eb84c75c3a91" />


## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
