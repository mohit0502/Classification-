# Machine Learning Model Evaluation for Mobile Price Prediction

## Project Overview
This project focuses on evaluating and comparing different machine learning models to predict the price range of mobile devices. The dataset contains features related to mobile specifications and a target variable representing the price range.

## Key Features of the Dataset
- Number of samples: 2000
- Number of features: 21
- Features include specifications like RAM, battery power, screen dimensions, and more.
- Target variable: `price_range` (categorical with 4 levels: 0, 1, 2, 3)

## Models Implemented
1. **Logistic Regression**
2. **Support Vector Classifier (SVC)**
3. **Random Forest**
4. **Ensemble Voting Classifier**

## Steps Performed
1. **Data Analysis and Preprocessing**:
   - Checked for null values and distributions.
   - Scaled features for models sensitive to feature scaling (e.g., Logistic Regression and SVC).
   - Identified RAM as the feature with the highest correlation to the target.

2. **Hyperparameter Tuning**:
   - Used GridSearchCV to optimize parameters for Logistic Regression, SVC, and Random Forest.
   - Explored parameters like regularization (`C`), number of estimators (`n_estimators`), max depth (`max_depth`), and more.

3. **Model Evaluation**:
   - Calculated metrics: Accuracy, Precision, Recall, and F1-score for training, validation, and test sets.
   - Used SHAP values for feature importance analysis in the Random Forest model.

4. **Ensemble Modeling**:
   - Combined the predictions of Logistic Regression, SVC, and Random Forest using hard and soft voting to improve accuracy.

## Results
| Model               | Training Accuracy | Validation Accuracy | Test Accuracy |
|---------------------|-------------------|---------------------|---------------|
| Logistic Regression | 98%              | 98%                 | 97%           |
| SVC                 | 98%              | 98%                 | 97%           |
| Random Forest       | 99%              | 85%                 | 88%           |
| Ensemble Model      | 98%              | 98%                 | 98%           |

## Dependencies
- Python 3.11.4
- Libraries:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - scikit-learn
  - shap

## Visualizations
- Correlation heatmaps for feature relationships.
- SHAP beeswarm plots for feature importance analysis.
- Line and bar plots to analyze hyperparameter effects.

## Acknowledgments
This project demonstrates model evaluation techniques for classification problems and serves as a reference for hyperparameter tuning and ensemble modeling.

---

Feel free to adapt this content to fit your specific project requirements!
