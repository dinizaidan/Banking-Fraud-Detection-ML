# Banking Fraud Detection using Machine Learning
This project compares multiple supervised machine learning algorithms for detecting fraudulent retail banking transactions using Python and Scikit-learn.
The project covers the complete machine learning pipeline, including exploratory data analysis, data preprocessing, feature engineering, model training, hyperparameter tuning, and performance evaluation. Logistic Regression, Decision Tree, and Random Forest are compared to determine the most effective model for fraud detection.

## Project at a Glance
| Item | Details |
|------|---------|
| Problem | Fraud Detection |
| Dataset | Retail Banking Fraud Dataset |
| Records | 10,000 |
| Features | 20 |
| Task | Binary Classification |
| Models | Logistic Regression, Decision Tree, Random Forest |
| Best Model | Logistic Regression |
| ROC-AUC | 0.9797 |
| Language | Python |

## Project Overview
Financial fraud poses significant challenges for banking institutions due to increasing transaction volumes and evolving fraud patterns. This project evaluates three supervised machine learning algorithms to classify banking transactions as fraudulent or legitimate. The study compares model performance using multiple evaluation metrics and investigates the impact of feature engineering and hyperparameter tuning on fraud detection accuracy.

## Repository Structure
```
Banking-Fraud-Detection-ML
│
├── notebooks/
├── images/
├── docs/
├── data/
├── README.md
├── LICENSE
└── requirements.txt
```

## Dataset
The dataset used in this project is publicly available on Kaggle.
| Attribute | Value |
|------------|-------|
| Source | [Kaggle Dataset](https://www.kaggle.com/datasets/deepeshkansotia/banking-fraud-detection-and-risk-analytics-dataset) |
| Records | 10,000 |
| Features | 20 |
| Target | Fraud Flag |
| Task | Binary Classification |

## Methodology
![Methodology Workflow](Images/Workflow.jpeg)
The project follows a complete machine learning workflow beginning with data understanding and preprocessing, followed by feature engineering and exploratory data analysis. Three classification models were developed and evaluated using multiple performance metrics. The best-performing model was then optimized using `GridSearchCV` to produce the final fraud detection model.

## Exploratory Data Analysis (EDA)
Before model development, EDA was conducted to better understand the dataset, identify potential issues, and examine relationships between variables.

### Fraud Distribution
![Fraud Distribution](Images/FraudFlag.png)
The bar chart show how the target in this data is imbalance. 

### Correlation Heatmap
![Correlation Heatmap](Images/CorrelationHeatmap.png)
The correlation heatmap was used to examine relationships between numerical features and identify potential multicollinearity. Understanding feature correlations helps guide feature selection and model interpretation.

### Outlier Analysis
![Outlier Analysis](Images/OutlierBotplox.png)
Boxplots were used to visualize the distribution of numerical variables and detect potential outliers. This analysis provides insight into data variability and supports decisions during preprocessing.

## Feature Engineering
Feature engineering and feature selection were performed to identify the most informative variables for fraud detection. Mutual Information was used to measure the dependency between each feature and the target variable.

### Top Features Based on Mutual Information
![Mutual Information](Images/FeatureImportance.png)
The ranking highlights the features that contributed most to distinguishing fraudulent and legitimate transactions.

## Machine Learning Models
| Model |	Why it was chosen |
|------:|------------------:|
| Logistic Regression |	Baseline linear classifier with good interpretability |
| Decision Tree	| Captures non-linear decision boundaries |
| Random Forest	| Ensemble model that reduces overfitting and improves predictive performance |

## Model Evaluation
**Model Performance**
| Model | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|-------|---------:|----------:|-------:|---------:|--------:|
| Logistic Regression | 0.9257 | 0.6357 | **0.9493** | 0.7615 | **0.9789** |
| Random Forest | **0.9433** | **0.8042** | 0.7227 | 0.7612 | 0.9742 |
| Decision Tree | 0.9110 | 0.5906 | 0.9387 | 0.7250 | 0.9446 |

**ROC Comparison**
![ROC Comparison](Images/ROC_Comparison.png)

### Confusion Matrices
| Logistic Regression | Decision Tree | Random Forest |
|---------------------|---------------|---------------|
| ![](Images/ConfMatrix_LR.png) | ![](Images/ConfMatrix_DT.png) | ![](Images/ConfMatrix_RF.png) |

**Key Finding**
- Logistic Regression achieved the highest ROC-AUC score (0.9797).
- Feature engineering improved model performance.
- Class imbalance required careful evaluation using Recall and ROC-AUC rather than Accuracy alone.
- Logistic Regression was selected as the final model because it achieved the highest ROC-AUC and recall while remaining interpretable, making it well suited for fraud detection.

## Tech Stack
Python | Pandas | NumPy | Scikit-learn | Matplotlib | Google Colab

## Documentation
- [Project Report](docs/Mini Project ML.pdf)
- [Project Summary](docs/Project_Summary.pdf)

## Contact
For any questions or feedback: dininadwah@gmail.com / [linkedin](https://www.linkedin.com/in/dznadwah/)
