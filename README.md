# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner


## Algorithm (Multivariate Linear Regression)

### Step 1

Read the input dataset containing independent variables (features) and dependent variable (target).

### Step 2

Initialize the parameters (weights and bias) with zeros or small random values.

### Step 3

Compute the predicted output using the hypothesis function:
( Y_{pred} = XW + b )

### Step 4

Calculate the error and cost function (Mean Squared Error).

### Step 5

Update the parameters (weights and bias) using gradient descent to minimize the error.

### Step 6

Repeat Steps 3–5 until convergence or for a fixed number of iterations.

### Step 7

Display the final weights, bias, and predicted output.

## Program:
```
import pandas as pd
from sklearn.linear_model import LinearRegression

# Load dataset
df = pd.read_csv("carsemission.csv")

# Select features and target
X = df[['Weight', 'Volume']]
y = df['CO2']

# Create and train model
model = LinearRegression()
model.fit(X, y)

# Print model parameters
print("Coefficients:", model.coef_)
print("Intercept:", model.intercept_)

# Predict for new data
new_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
prediction = model.predict(new_data)

print("Predicted CO2:", prediction)






```
## Output:

<img width="882" height="655" alt="image" src="https://github.com/user-attachments/assets/ea23065b-1fb9-4177-a8fd-7e53aa535b59" />


<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
