# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee
### NAME: KEERTHANA V
### REG NO: 212223220045

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:
1.Import the libraries and read the data frame using pandas

2.Calculate the null values present in the dataset and apply label encoder.

3.Determine test and training data set and apply decison tree regression in dataset.

4.calculate Mean square error, data prediction and r2. 
 

## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: KEERTHANA V
RegisterNumber: 212223220045
```
```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
```
## Output:
![image](https://github.com/user-attachments/assets/5f4a444a-c208-4b4f-b131-811029c5ed73)

```
data.info
```
## Output:
![image](https://github.com/user-attachments/assets/83142d74-3ce8-4089-8f80-3966d3b150aa)
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
```
## Output:
![image](https://github.com/user-attachments/assets/d82d5d7d-37e4-4272-a47a-52c2653994c9)

```
x=data[["Position","Level"]]
y=data[["Salary"]]
```
```
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)
```
```
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
```
```
from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse
```
## Output:
![image](https://github.com/user-attachments/assets/aec77c9d-89da-4d01-ba29-2fd247f6da74)
```
r2=metrics.r2_score(y_test,y_pred)
r2
```
## Output:
![image](https://github.com/user-attachments/assets/287b45c3-6db1-43fe-a73e-e765766434f2)
```
dt.predict([[5,6]])
```
## Output:
![image](https://github.com/user-attachments/assets/5e2cc940-3abe-4503-a3d8-7fb83cbe1b06)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
