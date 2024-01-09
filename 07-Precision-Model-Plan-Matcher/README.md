# Precision-Model-Plan-Matcher

## Megaline Plan Matcher: Precision Model for Subscriber Plan Recommendation

### Project Description

Mobile carrier Megaline has found out that many of their subscribers use legacy plans. They want to develop a model that would analyze subscribers' behavior and recommend one of Megaline's newer plans: Smart or Ultra. By accessing the behavior data about subscribers who have already switched to the new plans, it is possible to develop a model that will pick the right plan. The data preprocessing step has been completed in the previous Statistical Data Analyis, so we can now create the model to prediction this outcome witht he highets possible accuracy.  Since the outcomes are categorical, with two possibilities, either Smart or Ultra, the focus will be on creating a Classification algorithm model. 

**Key Objectives:**

- Develop a classification model that accurately predicts whether a subscriber should be recommended the Smart or Ultra plan.
- Achieve a model accuracy threshold of at least 0.75, ensuring that recommendations are reliable and effective.
- Validate the model's performance using a test dataset to confirm its real-world viability.

### Data description
Every observation in the dataset contains monthly behavior information about one user. 
The information given is as follows: 
- сalls — number of calls,
- minutes — total call duration in minutes,
- messages — number of text messages,
- mb_used — Internet traffic used in MB,
- is_ultra — plan for the current month (Ultra - 1, Smart - 0).

### Process
 - Split the source data into a training set, a validation set, and a test set.
- Investigate the quality of different models by changing hyperparameters
- Check the quality of the model using the test set.
- Sanity check the model.

In conclusion, the sanity check performed using the DummyClassifier with the 'most_frequent' strategy, provides a way to evaluate the performance of the model. The purpose of the sanity check is to ensure that any subsequent models developed are able to learn meaningful patterns and perform better than random approaches. The check returned 69% mean accuracy on the test, meaning that approximately 69% of the predictions made by the model align with the actual class labels in the test set.
