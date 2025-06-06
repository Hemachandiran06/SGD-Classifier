# SGD-Classifier
## AIM:
To write a program to predict the type of species of the Iris flower using the SGD Classifier.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import required libraries like sklearn, pandas, and matplotlib.

2.Load the Iris dataset and convert it into a DataFrame.

3.Split the data into features (X) and target (Y).

4.Divide data into training and testing sets.

5.Train the model using SGDClassifier on the training data.

6.Predict and evaluate using accuracy score and confusion matrix.

## Program:
```
/*
Program to implement the prediction of iris species using SGD Classifier.


import pandas as pd
from sklearn.datasets import load_iris
from sklearn.linear_model import SGDClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score, confusion_matrix
import matplotlib.pyplot as plt
import seaborn as sns

# Load the Iris dataset
iris = load_iris()
df = pd.DataFrame(data=iris.data, columns=iris.feature_names)
df['target'] = iris.target
print(df.head())

# Split features and target
x = df.drop('target', axis=1)
y = df['target']

# Train-test split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=42)

# Initialize and train SGD classifier
sgd_clf = SGDClassifier(max_iter=1000, tol=1e-3)
sgd_clf.fit(x_train, y_train)

# Predict and evaluate
y_pred = sgd_clf.predict(x_test)
accuracy = accuracy_score(y_test, y_pred)
print(f"Accuracy: {accuracy:.3f}")

# Confusion matrix
cf = confusion_matrix(y_test, y_pred)
print("Confusion Matrix:\n", cf)

# Optional: visualize confusion matrix
sns.heatmap(cf, annot=True, fmt='d', cmap='Blues', xticklabels=iris.target_names, yticklabels=iris.target_names)
plt.title('Confusion Matrix')
plt.xlabel('Predicted')
plt.ylabel('Actual')
plt.show()

*/
```

## Output:
## DATASET
![Screenshot 2025-04-16 221413](https://github.com/user-attachments/assets/ff71bfa6-6e3f-4a89-8a75-a1d2a4be05fa)

## TRAIN SGC CLASSIFIER
![Screenshot 2025-04-16 221521](https://github.com/user-attachments/assets/e1ca07e8-1a16-45ce-88d7-edd559d9895a)

## PREDICTIONS AND EVALUATE
![Screenshot 2025-04-16 221544](https://github.com/user-attachments/assets/cd230832-3dca-4719-9b6d-cc6783dd1b9a)

## CONFUSION MATRIX
![Screenshot 2025-04-16 221700](https://github.com/user-attachments/assets/62575372-d3c4-476f-8e1d-c3b33cf2a307)

## Developed by : HEMACHANDIRAN J
## Reg no: 24900182


## Result:
Thus, the program to implement the prediction of the Iris species using SGD Classifier is written and verified using Python programming.
