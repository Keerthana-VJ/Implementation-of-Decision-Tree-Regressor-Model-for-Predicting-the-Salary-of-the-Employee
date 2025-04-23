# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
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


## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
