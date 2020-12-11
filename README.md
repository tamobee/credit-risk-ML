# Risky Business

![Credit Risk](Images/credit-risk.jpg)

## Background
In order to mitigate risk, I built and evaluated several machine-learning models to predict credit risk using free data from LendingClub.
I employed the *imbalanced-learn* and *Scikit-learn* libraries to build and evaluate models using the two following techniques:

1. [Resampling](#Resampling)
2. [Ensemble Learning](#Ensemble-Learning)

### Files
    
* [Resampling Notebook](Code/credit_risk_resampling.ipynb)

* [Ensemble Notebook](Code/credit_risk_ensemble.ipynb)

* [Lending Club Loans Data](Resources/LoanStats_2019Q1.csv.zip)

---

### Resampling

For this approach, I used the [imbalanced learn](https://imbalanced-learn.readthedocs.io) library to resample the LendingClub data; built and evaluated logistic regression classifiers using the resampled data.    
*Refer to: [Resampling Notebook](Code/credit_risk_resampling.ipynb)*

#### Conclusion
1. Which model had the best balanced accuracy score?

    *SMOTEENN had the best balanced accuracy score of `0.7975462408998795`      
    versus `0.7752245065690078`; `0.7966770207605626`; `0.7856360112968401`      
    for Cluster Centroids, SMOTE, and Random Oversampler respectively.*

2. Which model had the best recall score?

    *SMOTE had the best recall score: `0.88`.*

3. Which model had the best geometric mean score?

    *SMOTEENN had the best geometric mean score: `0.79`.*
    
---

### Ensemble Learning

For this method, I trained and compared two different ensemble classifiers to predict loan risk and evaluate each model. I used the [Balanced Random Forest Classifier](https://imbalanced-learn.readthedocs.io/en/stable/generated/imblearn.ensemble.BalancedRandomForestClassifier.html#imblearn-ensemble-balancedrandomforestclassifier) and the [Easy Ensemble Classifier](https://imbalanced-learn.readthedocs.io/en/stable/generated/imblearn.ensemble.EasyEnsembleClassifier.html#imblearn-ensemble-easyensembleclassifier). For the ensemble learners, I used 100 estimators (`n_estimators=100`) for both models.    
*Refer to: [Ensemble Notebook](Code/credit_risk_ensemble.ipynb)*

#### Conclusion
1. Which model had the best balanced accuracy score?

    *Easy Ensemble Classifier had the best balanced accuracy score: `0.931601605553446`      
    versus `0.7855345052746622` for Balanced Random Forest Classifier.*
    
2. Which model had the best recall score?

    *Easy Ensemble Classifier had the best recall score: `0.94` versus      
    `0.90`for Balanced Random Forest Classifier.*
    
3. Which model had the best geometric mean score?

    *Easy Ensemble Classifier had the best geometric mean score: `0.93` versus      
    `0.78` for Balanced Random Forest Classifier.*
    
4. What are the top three features?

    *Top three features are the following:   
    `(0.09175752102205247, 'total_rec_prncp'),    
    (0.06410003199501778, 'total_pymnt_inv'),    
    (0.05764917485461809, 'total_pymnt')`*