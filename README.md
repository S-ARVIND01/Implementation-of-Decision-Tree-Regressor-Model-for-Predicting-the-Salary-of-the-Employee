# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard libraries. 2.Upload the dataset and check for any null values using .isnull() function.
2. Import LabelEncoder and encode the dataset.
3. Import DecisionTreeRegressor from sklearn and apply the model on the dataset.
4. Predict the values of arrays.
5. Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset 7.Predict the values of array.
6. Apply to new unknown values.

## Program:

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

Developed by: ARVIND S

RegisterNumber:  212222240012

```python
import pandas as pd
data=pd.read_csv("Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
y=data["Salary"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
```

## Output:
### data.head():
![Screenshot 2023-10-13 095739](https://github.com/S-ARVIND01/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707337/6ddb0d5b-c108-44b0-82cc-8674d50a6296)

###  data.info():
![Screenshot 2023-10-13 093023](https://github.com/S-ARVIND01/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707337/9fcea6e9-ef08-41b4-9927-9463363494e1)

### isnull() & sum() function:
![Screenshot 2023-10-13 093051](https://github.com/S-ARVIND01/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707337/c3a5ac4a-6618-4338-8a2b-147b66caed79)

### data.head() for Position:
![Screenshot 2023-10-13 094656](https://github.com/S-ARVIND01/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707337/9613b64b-c5af-40de-b0e9-7ce51b705e66)

### MSE value:
![Screenshot 2023-10-13 094743](https://github.com/S-ARVIND01/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707337/af7810e2-aff2-431c-b542-eb77e6c4fde5)

### R2 value:
![Screenshot 2023-10-13 094830](https://github.com/S-ARVIND01/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707337/e7cfae1f-c341-4c5f-8f7c-e4e6558a0fa3)

### Prediction value:
![Screenshot 2023-10-13 094957](https://github.com/S-ARVIND01/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/118707337/cbe9e251-7eb9-42e2-8d3a-f5afba5bf616)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
