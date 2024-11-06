# Medical Cost Prediction
&emsp;The [dataset](https://github.com/stedy/Machine-Learning-with-R-datasets/blob/master/insurance.csv) contains `1338` individuals' information with `6` attributes. They are `age`, `sex`, `BMI`, `number of children`, `whether is a smoker`, `residential region`. The outcome variable is the medical cost. This project showed a promising predictive **linear regression** model for estimating medical cost. It can be useful for insurance companies and government to determine policy cost and to allocate resources respectively. 

&emsp;Eventually, after conducting **exploratory data analysis** and **feature engineering**, a new feature was created that may be related to `hospital choice`. Together with `age` and `whether is a smoker`, a regression model with approximately 96.6% accuracy was built.

&emsp;Future work requires researching about the exact feature that was created. 

# Exploratory Data Analysis
The important parts of the exploratory data analysis are listed in the following.

## Categorical Features
![Categorical Features](https://github.com/moscmh/medicalcost/blob/main/plot/categorical.png?raw=true)
* `Sex` and `residential region` were found to have no significant relationship with `medical cost`.
* `Whether a smoker` showed a significant difference in medical cost between smokers and non-smokers.

## Numeric Features
![Numeric Features](https://github.com/moscmh/medicalcost/blob/main/plot/numeric.png?raw=true)
* Three scatterplots were shown to examine the relationships of `Age` and `BMI` with `medical cost`.
* `BMI` did not show a linear relationship with `medical cost`.
* There were three trendlines in the scatterplot for `medical cost` vs `age`. Clustering was conducted next to efficiently label the three different groups.

## Feature Engineering
![Feature engineering](https://github.com/moscmh/medicalcost/blob/main/plot/feature_engineering.png?raw=true)
* **Guassian Mixture Model** was used to efficiently cluster the individuals from the three trendlines respectively.
* The trendlines could be explained by the choice of hospitals.

# Model Training and Result
* Eventually, `age`, `BMI`, 
