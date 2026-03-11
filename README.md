# BLENDED_LEARNING
# Implementation of Decision Tree Model for Tumor Classification

## AIM:
To implement and evaluate a Decision Tree model to classify tumors as benign or malignant using a dataset of lab test results.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. **Load Data**  
   Import the dataset to initiate the analysis.

2. **Explore Data**  
   Examine the dataset to identify patterns, distributions, and relationships.

3. **Select Features**  
   Determine the most important features to enhance model accuracy and efficiency.

4. **Split Data**  
   Separate the dataset into training and testing sets for effective validation.

5. **Train Model**  
   Use the training data to build and train the model.

6. **Evaluate Model**  
   Measure the model’s performance on the test data with relevant metrics.


## Program:
```
/*
Program to  implement a Decision Tree model for tumor classification.
Developed by: A PRAVEEN KISHORE
RegisterNumber: 212225220074

import pandas as pd 
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix
import seaborn as sns
import matplotlib.pyplot as plt

data = pd.read_csv('tumor.csv')
print(data.head())
print(data.columns)

X = data.drop(columns=['Class'])  
y = data['Class']

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)

model= DecisionTreeClassifier(random_state=42)
model.fit(X_train,y_train)

y_pred=model.predict(X_test)

acc=accuracy_score(y_test,y_pred)
classi=classification_report(y_test,y_pred)
print('Accuracy=',acc)
print()
print('----Classification Report----')
print(classi)

con=confusion_matrix(y_test,y_pred)
sns.heatmap(con,annot=True,fmt='d',cmap='Blues')
plt.xlabel('Predicted')
plt.ylabel('Actual')
plt.show()
*/
```

## Output:
<img width="591" height="260" alt="1" src="https://github.com/user-attachments/assets/aae0369c-f7ce-4653-8b1c-544bb497c223" />
<img width="732" height="542" alt="2" src="https://github.com/user-attachments/assets/6fd8f3f4-053b-4536-a1a4-ca04e2989c11" />




## Result:
Thus, the Decision Tree model was successfully implemented to classify tumors as benign or malignant, and the model’s performance was evaluated.
