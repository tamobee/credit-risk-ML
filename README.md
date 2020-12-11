# Risky Business

![Credit Risk](Images/credit-risk.jpg)

## Background

I used the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the two following techniques:

1. [Resampling](#Resampling)
2. [Ensemble Learning](#Ensemble-Learning)

### Resampling

#### Conclusion
1. Which model had the best balanced accuracy score?

    *SMOTEENN had the best balanced accuracy score.*
    
3. Which model had the best recall score?

    *SMOTE had the best recall score.*
    
4. Which model had the best geometric mean score?

    *SMOTEENN had the best geometric mean score.*

### Ensemble Learning

#### Conclusion
1. Which model had the best balanced accuracy score?

    *EasyEnsembleClassifier had the best balanced accuracy score.*
    
2. Which model had the best recall score?

    *EasyEnsembleClassifier had the best recall score*
    
3. Which model had the best geometric mean score?

    *EasyEnsembleClassifier had the best geometric mean score*
    
4. What are the top three features?

    *Top 3 features are the following: 
    (0.09175752102205247, 'total_rec_prncp'), 
    (0.06410003199501778, 'total_pymnt_inv'),
    (0.05764917485461809, 'total_pymnt')*