# Heart Disease Data Integration and KNN Classification

Heart disease remains one of the leading causes of mortality globally. Early detection and prevention are critical in reducing mortality rates. This project aims to leverage machine learning techniques to predict the likelihood of heart disease in patients based on clinical attributes. The project utilizes the K-Nearest Neighbors (KNN) classification algorithm, a robust instance-based learning method suitable for medical datasets where similar patient profiles often share similar diagnostic outcomes.

## Dataset

The project utilizes the Heart Disease Dataset sourced from the UCI Machine Learning Repository. The dataset includes a mix of numerical, binary, and categorical features representing clinical indicators such as:


+ Numerical: Age, Resting Blood Pressure (trestbps), Serum Cholesterol (chol), Maximum Heart Rate (thalach), ST Depression (oldpeak).
+ Categorical/Binary: Sex, Chest Pain Type (cp), Fasting Blood Sugar (fbs), Resting ECG (restecg), Exercise Induced Angina (exang), Slope of Peak Exercise ST Segment (slope), Number of Major Vessels (ca), Thalassemia (thal).
+ Target Variable: Presence (1) or absence (0) of heart disease.

## Methodology
### 3.1 Data Preprocessing:
Data preprocessing was a critical phase to ensure data quality and model accuracy. The following steps were implemented using Python (Pandas, NumPy):
+ Data Loading
+ Handling Missing Values using Manual KNN Imputation
+ Outlier Removal using the Interquartile Range (IQR) method
+ Normalization using Min-Max Scaling
+ Data Splitting

### 3.2 Exploratory Data Analysis (EDA)
Comprehensive EDA was conducted to understand feature distributions, relationships, and data quality. The following visualizations were generated using Matplotlib and Seaborn:
+ Visualizing distributions (Histogram, Boxplot, Q-Q Plot)
+ Analyzing relationships (Correlation Matrix, Pairplot)
+ Categorical distribution analysis (Count Plots).

### 3.3 Classification Using K-Nearest Neighbors (KNN)
A custom KNN classifier was implemented to handle the mixed data types (numerical and categorical) effectively.
+ Distance Metric
###### Euclidean Distance: Used for numerical features (age, chol, etc.)
###### Hamming Distance: Used for categorical features (sex, cp, etc.).
+ Hyperparameter Tuning
+ Evaluation Metrics

### 4. Results and Performance
Calculating Accuracy, Precision, Recall, and F1-Score.
+ Performance Metrics (for K=3):
###### Accuracy: 93%
###### Precision: 96%
###### Recall: 90%
###### F1-Score: 93%

+ Confusion Matrix Analysis

## Project Structure
```
KNN/
│
├── code.ipynb                # Main Jupyter Notebook containing the implementation
├── Dataset/
│   └── dataset.csv           # The UCI Heart Disease Dataset
├── README.md                 # Project documentation
```

## References
1. UCI Machine Learning Repository: Heart Disease Data Set.
2. Detrano, R., et al. (1989). "International Application of a New Probability Algorithm for the Diagnosis of Coronary Artery Disease," American Journal of Cardiology.
3. Han, J., Kamber, M., & Pei, J. (2011). Data Mining: Concepts and Techniques (3rd ed.). Morgan Kaufmann.

Note: This project was developed as part of a data mining course assignment.