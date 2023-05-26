# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required packages.
2. Read the data set.
3. Apply label encoder to the non-numerical column inoreder to convert into numerical values.
4. Determine training and test data set.
5. Apply decision tree regression on to the dataframe and get the values of Mean square error, r2 and data prediction.
## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: chadalawada jaswanth
RegisterNumber:  212221040030
```
```
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
x.head()

y=data[["Salary"]]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test, y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
```

## Output:
1. data.head()

![image](https://github.com/JayanthYadav123/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94836154/5b931a81-b2ff-4663-a974-26961522ab7f)

2. data.info()

![image](https://github.com/JayanthYadav123/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94836154/8edcbf1a-1e0f-4d75-90a8-5928c6b4dedc)

3. Null values

![image](https://github.com/JayanthYadav123/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94836154/76d5ec21-1bb5-45bb-9e37-6ea1e56a1c97)

4. data.head() for position
 
![image](https://github.com/JayanthYadav123/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94836154/fd491536-4fc8-40ad-89fd-629b59590d62)

5. x.head()
 
![image](https://github.com/JayanthYadav123/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94836154/089612ad-b6c7-4565-9358-08978ee9cd78)

6. Mean squared error(mse) value

![image](https://github.com/JayanthYadav123/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94836154/04e1e890-ded4-4f15-8fd3-2141dcf4d871)

7. r2 value

![image](https://github.com/JayanthYadav123/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94836154/3a846ff2-7a34-42a2-9bfb-bc59123c571e)

8. prediction value

![image](https://github.com/JayanthYadav123/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/94836154/809ad097-4bdf-462e-af71-0214de773fc6)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
