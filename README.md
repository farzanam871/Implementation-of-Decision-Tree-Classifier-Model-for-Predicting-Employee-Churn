# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
1.Import pandas
2.Import Decision tree classifier
3.Fit the data in the model
4.Find the accuracy score
```

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by:Lavanya R 
RegisterNumber:212225230149
*/
```
```
import numpy as np
from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score

X = np.array([
    [1, 20000, 2],
    [3, 30000, 3],
    [5, 50000, 4],
    [2, 25000, 2],
    [7, 70000, 5],
    [4, 40000, 3],
    [6, 60000, 4],
    [1, 22000, 1]
])

Y = np.array([1, 0, 0, 1, 0, 0, 0, 1])

X_train, X_test, Y_train, Y_test = train_test_split(X, Y, test_size=0.2, random_state=0)

model = DecisionTreeClassifier()
model.fit(X_train, Y_train)

Y_pred = model.predict(X_test)

print("Accuracy:", accuracy_score(Y_test, Y_pred))

sample = np.array([[3, 28000, 2]])
prediction = model.predict(sample)

print("Employee Churn Prediction (1=Leave, 0=Stay):", prediction[0])
```

## Output:
<img width="1265" height="92" alt="image" src="https://github.com/user-attachments/assets/4c8f56d0-1765-4909-b917-fcdf1151f486" />



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
