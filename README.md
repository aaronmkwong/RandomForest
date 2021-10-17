# Python-Random-Forest-Titanic-Survivorship

**_REPOSITORY UNDER CONSTRUCTION_**

This project uses Random Forest to classify a passenger's survivorship as died or survived. It uses the same engineered data and features as the  **[Logistic Regression Titanic Survivorship](https://github.com/aaronmkwong/Python-Logistic-Regression-Titanic-Survivorship)** project. Random Forests samples the training dataset with replacement (bagging), but trees are constructed in a way that reduces the correlation between individual classifiers (Brownlee, 2021, p.93) providing an improvement over Bagged Trees. Bagging (or Bootstrap Aggregation) takes multiple samples from the training dataset with replacement and trains a model for each sample, then averages the predictions of all sub-models to obtain a final averaged prediction (Brownlee, 2021, p. 92). The custom function rf_mod_assess() returns a dataframe of all of the classifcation report results for each of the 25 trials using Monte Carlo cross validation.  

See also the **[KNN Titanic Survivorship](https://github.com/aaronmkwong/Python-KNN-Titanic-Survivorship)** project.

The code can be viewed here: **[Titanic_Survivorship_Random_Forest_02.ipynb](https://github.com/aaronmkwong/Python-Random-Forest-Titanic-Survivorship/blob/main/Program%20Files/Titanic_Survivorship_Random_Forest_02.ipynb)**.  

**_Random Forest outperformed Logistic Regression and KNN by 2% and 1% respectively_**. 

<img src="https://github.com/aaronmkwong/Python-Random-Forest-Titanic-Survivorship/blob/main/Other%20Files/summary_results_01.JPG" width="750" height="75">

...

<img src="https://github.com/aaronmkwong/Python-Random-Forest-Titanic-Survivorship/blob/main/Other%20Files/top_mid_worst_results_02.JPG" width="700" height="175">

...

<img src="https://github.com/aaronmkwong/Python-Random-Forest-Titanic-Survivorship/blob/main/Other%20Files/feature_importance_01.JPG" width="500" height="400">

**REFERENCES**

Brownlee, Jason. (2021). *Machine Learning Mastery with Python: Understand Your Data, Create Accurate Models and Work Projects End-To-End* (v1.2 ed.). https://machinelearningmastery.com/machine-learning-with-python/
