# Practical-Homework-2-SVMs

This project investigates how behavioral and demographic variables relate to cancer diagnosis. Using machine learning on the 2022 National Health Interview Survey (NHIS), we apply Support Vector Machines (SVMs) to classify whether a respondent has ever been diagnosed with cancer. Given the imbalance in the dataset, class weighting is applied to improve detection of cancer-positive cases.

Theoretical Background
Support Vector Machines (SVMs) are supervised models that construct a hyperplane to separate classes with maximum margin. When data is not linearly separable, kernel functions are used to map inputs to higher-dimensional space.
Linear Kernel: Straight-line separation
Radial Basis Function (RBF): Flexible non-linear decision boundary
Polynomial Kernel: Higher-order curved separation
Class weighting helps address imbalanced datasets by penalizing misclassification of underrepresented classes more heavily.

# Methodology
Preprocessing:
Dropped invalid codes (e.g., 996–999).
Standardized predictors.
Stratified 80/20 train-test split.
Model Training:
Linear SVM (Cost = 1, manually set)
Radial SVM: 5-fold cross-validated hyperparameter tuning (C, Gamma)
Polynomial SVM: 5-fold cross-validated hyperparameter tuning (C, Degree)
Applied class weighting to handle imbalance: class.weights = c(\"No\"=1, \"Yes\"=5)
