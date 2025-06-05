# -Support-Vector-Machines-SVM-
Breast Cancer Classification using Support Vector Machines (SVM)
Project Overview
This project demonstrates how to build a simple machine learning classifier to predict breast cancer diagnosis (malignant or benign) based on tumor features. The classification is done using Support Vector Machines (SVM) — a powerful and popular supervised learning algorithm.

Dataset
The dataset used is a breast cancer dataset containing various features extracted from digitized images of breast mass samples. Each record represents a tumor with numeric features such as radius, texture, perimeter, area, and others, along with a diagnosis label:

Diagnosis: Malignant (M) or Benign (B)

Features: Numeric values describing the tumor characteristics (e.g., radius_mean, texture_mean, etc.)

The dataset is loaded from a CSV file named breast-cancer.csv.

Steps Followed
1. Data Loading and Exploration
The dataset is read using pandas.

The first few rows and column names are printed for inspection.

Missing data is dropped to ensure clean input.

2. Feature and Target Selection
Two numeric features, radius_mean and texture_mean, are selected for classification.

The target variable diagnosis is mapped to numeric values: malignant tumors labeled as 1, benign as 0.

3. Data Preprocessing
The dataset is split into training and testing sets with a 70-30 ratio.

Features are standardized using StandardScaler to normalize the data for better SVM performance.

4. Model Training and Visualization
A Linear SVM model is trained on the scaled training data, and its decision boundary is plotted to visualize how it separates the two classes.

An RBF (Radial Basis Function) kernel SVM is also trained, providing a nonlinear decision boundary, and visualized similarly.

5. Model Evaluation
The RBF SVM model is evaluated on the test data.

Metrics such as accuracy, confusion matrix, and a detailed classification report (precision, recall, F1-score) are displayed.

6. Hyperparameter Tuning
Grid Search with cross-validation is performed to find the best combination of parameters (C, gamma) for the RBF kernel.

The best tuned model is visualized with its decision boundary.

7. Cross-Validation
The best model's robustness is further validated using 5-fold cross-validation on the training data.

Cross-validation accuracy scores and their mean are reported.

Key Takeaways
SVMs can efficiently classify breast cancer diagnosis with good accuracy using just two features.

Kernel methods like RBF allow modeling nonlinear boundaries for better separation.

Hyperparameter tuning improves model performance by selecting optimal settings.

Visualizing decision boundaries helps in understanding model behavior.
