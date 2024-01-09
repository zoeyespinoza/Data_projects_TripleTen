# Predictive-Modeling-for-Gold-Optimization

Predictive Modeling for Gold Recovery Optimization in Heavy Industry

# Project Description:

This project aims to develop a prototype of a machine learning model for Zyfra, a company specializing in efficiency solutions for heavy industry. The primary objective is to create a predictive model that can accurately estimate the amount of gold recovered from gold ore, using data on extraction and purification processes. By achieving this, Zyfra intends to optimize its production processes and eliminate unprofitable parameters, ultimately enhancing operational efficiency and profitability.

# Project Goals:

**Data Preparation**: Collect, clean, and preprocess the available data on gold extraction and purification. This step involves handling missing values, outlier detection, and data transformation to make it suitable for machine learning.

**Data Analysis**: Perform exploratory data analysis (EDA) to gain insights into the dataset. Visualize key features to understand the distribution, relationships, and patterns within the data.

**Model Development**: Build a machine learning model that predicts the amount of gold recovered from gold ore based on input features related to extraction and purification processes. The choice of the machine learning algorithm will be made after careful evaluation of the data and model requirements.

**Model Training**: Train the selected machine learning model using the preprocessed data. Employ techniques like cross-validation to assess model performance and fine-tune hyperparameters for optimal results.

# Data Description:
The data is stored in three files:
* gold_recovery_train.csv — training dataset 
* gold_recovery_test.csv — test dataset 
* gold_recovery_full.csv — source

# Technological Process:

How is gold extracted from ore? Let's look into the process stages.
Mined ore undergoes primary processing to get the ore mixture or rougher feed, which is the raw material for flotation (also known as the rougher process). After flotation, the material is sent to two-stage purification.
image
Let's break down the process:
1. **Flotation**
Gold ore mixture is fed into the float banks to obtain rougher Au concentrate and rougher tails (product residues with a low concentration of valuable metals).
The stability of this process is affected by the volatile and non-optimal physicochemical state of the flotation pulp (a mixture of solid particles and liquid).
2. **Purification**
The rougher concentrate undergoes two stages of purification. After purification, we have the final concentrate and new tails.

**Key Terms**
- Rougher feed — raw material
- Rougher additions (or reagent additions) — flotation reagents: Xanthate, Sulphate, Depressant
    - Xanthate — promoter or flotation activator;
    - Sulphate — sodium sulphide for this particular process;
    - Depressant — sodium silicate.
- Rougher process — flotation
- Rougher tails — product residues
- Float banks — flotation unit
- Cleaner process — purification
- Rougher Au — rougher gold concentrate
- Final Au — final gold concentrate

Parameters of stages

- air amount — volume of air
- fluid levels
- feed size — feed particle size
- feed rate

Feature naming: 
Here's how you name the features:
[stage].[parameter_type].[parameter_name]

Example: rougher.input.feed_ag

Possible values for [stage]:
- rougher — flotation
- primary_cleaner — primary purification
- secondary_cleaner — secondary purification
- final — final characteristics

Possible values for [parameter_type]:
- input — raw material parameters
- output — product parameters
- state — parameters characterizing the current state of the stage
- calculation — calculation characteristics

### Evaluation metric
To solve the problem, we will need a new metric, sMAPE, symmetric Mean Absolute Percentage Error. 

We need to predict two values:

- rougher concentrate recovery rougher.output.recovery
- final concentrate recovery final.output.recovery

## Conclusion
The best model for predicting the recovery rate of gold from gold ore is the Random Forest Regressor Model. The model achieved the best sMAPE score among all the models, indicating superior predictive performance. While the Decision Tree Regressor Model also performed well, the Random Forest Regressor Model outperformed it with a lower sMAPE score of 11.270081553781658. However, it's worth noting that the Random Forest Regressor Model took longer to run due to its complexity, but in the deployed model, we mostly care about prediction time, not training time.

After creating and training the Random Forest Regressor model, we applied it to make predictions on the test data while handling missing values appropriately. By excluding data points with missing target values and evaluating the model on a valid subset, we obtained a reliable sMAPE score.

The sMAPE score for the Random Forest Regressor Model further confirms its success. However, it's essential to address the observation that our best model performed worse than the constant baseline. Several factors could contribute to this, such as data quality issues, or the presence of hidden variables that we don't have access to, influencing the target variable. While the Random Forest Regressor Model demonstrated better predictive power, the challenges in achieving accurate predictions indicate the need for further investigation and data refinement to enhance model performance. Considering both predictive accuracy and computational efficiency, the Random Forest Regressor Model remains the preferred choice for predicting the recovery rate of gold from gold ore, but further efforts should be directed toward refining the model and data collection processes to improve its reliability.
