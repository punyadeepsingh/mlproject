## End to End Machine Learning Project




EDA: Student Performance Analysis
 Project Title
Student Performance Indicator
Analyzing factors affecting student exam scores using data analysis and visualization.

 Problem Statement
The goal of this project is to understand how student performance is influenced by:


Gender


Race/Ethnicity


Parental level of education


Lunch type


Test preparation course


We analyze their impact on:


Math score


Reading score


Writing score



 Dataset Information


Source: Kaggle – Students Performance in Exams


Total Records: 1000 students


Total Features: 8 columns


Features include:
CategoryColumnsDemographicgender, race_ethnicityFamily Backgroundparental_level_of_educationSupport Factorslunch, test_preparation_courseAcademic Scoresmath_score, reading_score, writing_score

 Data Quality Checks
✔ No missing values
✔ No duplicate records
✔ Correct data types
✔ Balanced categorical distributions
This means the dataset is clean and reliable for analysis.

 Numerical Summary
MetricMathReadingWritingMean66.0969.1768.05Std Dev15.1614.6015.19Min01710Max100100100
Insight:
Average scores are close across all subjects, but Math has the lowest minimum, showing some students struggle heavily there.

 Feature Types


Numerical Features (3):
Math, Reading, Writing scores


Categorical Features (5):
Gender, Race/Ethnicity, Parental Education, Lunch, Test Prep Course



 New Features Created
Two new performance indicators were added:


Total Score = Math + Reading + Writing


Average Score = Total Score / 3


These help measure overall academic performance.

 Performance Extremes
Full Marks (100):


Math: 7 students


Reading: 17 students


Writing: 14 students


Below 20 Marks:


Math: 4 students


Reading: 1 student


Writing: 3 students


Insight:
Students performed worst in Math and best in Reading overall.

 Score Distribution
(Use histogram/KDE plot)


Most students score in the 60–80 range


Distribution is roughly normal


Gender comparison shows performance spread across both groups



 Key EDA Conclusions
✔ Dataset is clean
✔ Reading scores are generally highest
✔ Math has more low scorers
✔ Parental education, lunch, and test prep likely influence performance
✔ Average score is a strong overall performance indicator


 Model Training: Predicting Math Scores
Slide 11 – Objective of Model
Build a Machine Learning model to predict Math Score based on:


Demographics


Parental education


Lunch type


Test preparation


Reading & Writing scores



Slide 12 – Feature & Target Selection


Target Variable (Y): Math Score


Input Features (X): All other columns



 Data Preprocessing
✔ Categorical features → One Hot Encoding
✔ Numerical features → Standard Scaling
✔ Final feature count after transformation: 19 features

 Train-Test Split


Training Data: 80% (800 students)


Testing Data: 20% (200 students)


Ensures fair model evaluation.

 Models Used
Multiple regression models were trained and compared:


Linear Regression


Ridge Regression


Lasso Regression


K-Nearest Neighbors


Decision Tree


Random Forest


XGBoost


CatBoost


AdaBoost



 Evaluation Metrics
Models were evaluated using:


MAE – Mean Absolute Error


RMSE – Root Mean Squared Error


R² Score – Accuracy of prediction



 Model Comparison (R² Score)
ModelR² ScoreRidge Regression0.8806Linear Regression0.8803CatBoost Regressor0.8516AdaBoost Regressor0.8498Random Forest0.8473Lasso0.8253XGBoost0.8216
🏆 Best Model: Ridge Regression

 Best Model Performance
Linear Regression (similar to Ridge):


RMSE: ~5.39


MAE: ~4.21


R² Score: 88% accuracy


This means predictions are very close to actual math scores.

 Actual vs Predicted Plot
(Use scatter + regression line plot)


Points lie close to diagonal line


Shows strong correlation between predicted and real scores


Model generalizes well on test data



 Final Conclusion
✔ Student performance can be predicted with high accuracy (88%)
✔ Reading & Writing scores strongly influence Math score
✔ Background factors also contribute
✔ Simple linear models performed as well as complex ensemble models



