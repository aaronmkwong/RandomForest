# Python-Random-Forest-Titanic-Survivorship

**_REPOSITORY UNDER CONSTRUCTION_**

This project uses Random Forest to classify a passenger's survivorship as died or survived. It uses the same engineered data and features as the  **[Logistic Regression Titanic Survivorship](https://github.com/aaronmkwong/Python-Logistic-Regression-Titanic-Survivorship)** project. Random Forests samples the training dataset with replacement (bagging), but trees are constructed in a way that reduces the correlation between individual classifiers (Brownlee, 2021, p.93) providing an improvement over Bagged Trees. Bagging (or Bootstrap Aggregation) takes multiple samples from the training dataset with replacement and trains a model for each sample, then averages the predictions of all sub-models to obtain a final averaged prediction (Brownlee, 2021, p. 92). The custom function rf_mod_assess() returns a dataframe of all of the classifcation report results for each of the 25 trials using Monte Carlo cross validation.  

See also the **[KNN Titanic Survivorship](https://github.com/aaronmkwong/Python-KNN-Titanic-Survivorship)** project.

The code can be viewed here: **[Titanic_Survivorship_Random_Forest_02.ipynb](https://github.com/aaronmkwong/Python-Random-Forest-Titanic-Survivorship/blob/main/Program%20Files/Titanic_Survivorship_Random_Forest_02.ipynb)**.  

**_Random Forest outperformed Logistic Regression and KNN by 2% and 1% respectively_**. 

<img src="https://github.com/aaronmkwong/Python-Random-Forest-Titanic-Survivorship/blob/main/Other%20Files/summary_results_01.JPG" width="750" height="75">

To determine the feature importance the middle result random state 19 is used. 

<img src="https://github.com/aaronmkwong/Python-Random-Forest-Titanic-Survivorship/blob/main/Other%20Files/top_mid_worst_results_02.JPG" width="700" height="175">

Permutation Importance rather than Random Forest Feature Importance is used since the latter suffers from being computed on statistics derived from the training dataset (Scikit-Learn, 2021a). The permutation feature importance is defined to be the decrease in a model score when a single feature value is randomly shuffled, which breaks the relationship between the feature and the target, thus the drop in the model score is indicative of how much the model depends on the feature (Scikit-Learn, 2021b). In the boxplot below accuracy is used for scoring the model. 

<img src="https://github.com/aaronmkwong/Python-Random-Forest-Titanic-Survivorship/blob/main/Other%20Files/feature_importance_01.JPG" width="500" height="400">

**REFERENCES**

Brownlee, Jason. (2021). *Machine Learning Mastery with Python: Understand Your Data, Create Accurate Models and Work Projects End-To-End* (v1.2 ed.). https://machinelearningmastery.com/machine-learning-with-python/

Scikit-Learn. (2021a, October 17). https://scikit-learn.org/stable/auto_examples/inspection/plot_permutation_importance.html#sphx-glr-auto-examples-inspection-plot-permutation-importance-py

Scikit-Learn. (2021b, October 17). https://scikit-learn.org/stable/modules/permutation_importance.html#permutation-importance
