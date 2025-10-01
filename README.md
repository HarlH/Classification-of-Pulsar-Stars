# Classification of Pulsar Stars  

This project explores machine learning techniques to classify pulsar stars vs non-pulsars using the HTRU2 dataset. The goal is to build and evaluate predictive models and interpret what features drive classification performance.

---

## 📌 Project Overview

Pulsars are highly magnetized rotating neutron stars that emit beams of electromagnetic radiation. The HTRU2 dataset provides measurements from radio telescopes that can help distinguish pulsars from non-pulsars.

In this project, I:

- Preprocessed and cleaned the dataset  
- Explored feature distributions, correlations, and class imbalance  
- Built and compared multiple classifiers (e.g. Random Forest, Support Vector Machine)  
- Tuned hyperparameters and validated performance  
- Analyzed feature importance and model explainability  

---

## 🧮 Dataset & Features

- **Dataset:** HTRU2 (available from UCI / astrophysics repositories)  
- **Observations / Instances:** ~17,898 samples (exact number after cleaning)  
- **Features (eight continuous variables):**  
  1. Mean of the integrated profile  
  2. Standard deviation of the integrated profile  
  3. Excess kurtosis of integrated profile  
  4. Skewness of integrated profile  
  5. Mean of the DM-SNR curve  
  6. Standard deviation of the DM-SNR curve  
  7. Excess kurtosis of DM-SNR curve  
  8. Skewness of DM-SNR curve  

- **Target:** Binary label: `pulsar` (1) or `non-pulsar` (0)

---

## 🛠️ Methodology & Workflow

1. **Data Preprocessing**  
   - Checked for missing values, anomalies  
   - Scaled numeric features (StandardScaler / MinMax)  
   - Handled class imbalance (e.g. resampling, class weights)  

2. **Exploratory Data Analysis (EDA)**  
   - Feature histograms, boxplots, pair plots  
   - Correlation matrix to check multicollinearity  
   - Visualizing class separability  

3. **Model Building & Tuning**  
   - Baseline models: logistic regression, decision tree  
   - Advanced models: Random Forest, SVM  
   - Hyperparameter tuning via cross-validation / grid search  
   - Metrics: Accuracy, Precision, Recall, F1-score, ROC-AUC  

4. **Evaluation & Interpretation**  
   - Confusion matrix and classification report  
   - ROC curve and AUC  
   - Feature importance / coefficient analysis  
   - Model limitations and error analysis  

---

## 📈 Key Results & Insights

- **Best Model Performance:**  
  - (e.g.) Random Forest achieved **X% accuracy**, with **ROC-AUC = Y**  
  - SVM gave competitive performance but with higher variance in cross-validation  

- **Feature Importance Highlights:**  
  - Features like (for example) *excess kurtosis of DM-SNR* and *mean of integrated profile* had strong predictive value  
  - Some features showed low importance and could potentially be dropped  

- **Challenges & Observations:**  
  - Class imbalance required careful handling (e.g. use of class weights or resampling)  
  - Some overlap in feature distributions between pulsar/non-pulsar made separation difficult  
  - Tuning hyperparameters was critical to achieving stable generalization  


