Aim
To study and implement Machine Learning Classification Algorithms using Python and analyze their performance on a dataset.
The objective is to understand the complete classification process including data loading, preprocessing, splitting the dataset, training models, prediction, and evaluating accuracy using different functions from Scikit-learn, Pandas, and NumPy libraries.

Theory
Introduction to Classification in Machine Learning
Classification is a supervised learning technique in which a model is trained using labeled data and then used to predict the category/class of new unseen data.

Examples:
Email → Spam / Not Spam
Student Result → Pass / Fail
Disease Detection → Positive / Negative
Loan Approval → Yes / No
The model learns patterns from input features and maps them to output labels.

Libraries Used in the Experiment
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

Theory of Libraries:
pandas
Used for handling datasets in tabular format.

numpy
Used for numerical operations and arrays.
matplotlib.pyplot
Used for plotting graphs and visualization.
seaborn
Used for advanced statistical data visualization.

Functions Used 
1. Reading Dataset
df = pd.read_csv("data.csv")
Function Used: pd.read_csv()
Used to load CSV files into a DataFrame.

Output:
Creates a table-like structure of rows and columns.

2. Display First Rows
df.head()
Function Used: head()
Displays first 5 rows of dataset.
Used to inspect data quickly.

3. Display Last Rows
df.tail()
Function Used: tail()

Displays last rows of dataset.

4. Shape of Dataset
df.shape
Function Used: shape

Returns:
(rows, columns)
Used to know dataset size.

5. Information of Dataset
df.info()
Function Used: info()

Displays:
Column names
Non-null values
Data types
Memory usage
6. Statistical Summary
df.describe()
Function Used: describe()

Returns:
Count
Mean
Std deviation
Minimum
Maximum
Quartiles

7. Checking Missing Values
df.isnull().sum()

Functions Used:
isnull()
Detects missing values.

sum()
Counts total null values column-wise.

8. Selecting Features and Target
X = df.drop('target', axis=1)
y = df['target']

Functions Used:
drop()
Removes specified column.

axis=1
Means column removal.

Data Splitting
from sklearn.model_selection import train_test_split
X_train,X_test,y_train,y_test = train_test_split(X,y,test_size=0.2,random_state=42)

Theory:
Dataset is divided into:
Training Data = Used to train model
Testing Data = Used to test model
Functions Used:
train_test_split()

Functions:
LogisticRegression()
Creates classification model.

fit(X_train,y_train)
Trains model using training data.

Prediction
y_pred = model.predict(X_test)

Function:
predict()
Predicts class labels for testing data.

Accuracy Evaluation
from sklearn.metrics import accuracy_score
accuracy_score(y_test,y_pred)
Function Used:
accuracy_score()

Confusion Matrix
from sklearn.metrics import confusion_matrix
confusion_matrix(y_test,y_pred)

Function Used:
confusion_matrix()

Shows:
True Positive
True Negative
False Positive
False Negative
Used for model evaluation.

Classification Report
from sklearn.metrics import classification_report
print(classification_report(y_test,y_pred))
Function Used:
classification_report()

Displays:
Precision
Recall
F1-score
Support
Other Classification Algorithms Possibly Used
Decision Tree
from sklearn.tree import DecisionTreeClassifier
model = DecisionTreeClassifier()

Used for rule-based classification.

K-Nearest Neighbors (KNN)
from sklearn.neighbors import KNeighborsClassifier
model = KNeighborsClassifier()

Classifies based on nearest data points.

Support Vector Machine (SVM)
from sklearn.svm import SVC
model = SVC()
Used to separate classes using hyperplane.
Visualization Functions
Heatmap
sns.heatmap(cm, annot=True)

Functions:
sns.heatmap()
Visualizes confusion matrix.
annot=True
Displays values inside boxes.
Plot Show
plt.show()
Displays graph output.


Conclusion
Thus, the experiment on Machine Learning Classification using Python was successfully performed. The dataset was loaded, explored, preprocessed, and divided into training and testing sets.
Classification models such as Logistic Regression / Decision Tree / KNN were trained and tested successfully. Various functions like read_csv(), head(), info(), describe(), train_test_split(), fit(), predict(), accuracy_score(),
confusion_matrix(), classification_report() were studied in detail. 
This experiment helped in understanding how classification models are built and evaluated for real-world prediction problems.
