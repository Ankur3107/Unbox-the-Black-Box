# Unbox-the-Black-Box

# OBJECTIVE

Actually I was thinking about ‘how to get the machine learning model explantion’. Then I searched on Google and found a great package called LIME by Tulio Ribeiro, Sameer Singh and Carlos Guestrin. I was very impressed with the package. In this kernel, I will share my knowledge that i got from different papers, blogs and videos.

# LIME : Locally Interpretable Model-agnostic Explanations

## ABSTRACT

Machine learning models remain mostly black boxes. Understanding the reasons behind predictions is, however, quite important in assessing trust, which is fundamental if one plans to take action based on a prediction, or when choosing whether to deploy a new model. Such understanding also provides insights into the model, which can be used to transform an untrustworthy model or prediction into a trustworthy one.

## WHAT IS LIME

* **Locally**: Locally faithful to the classifier
* **Interpretable**: Representation that is understandable to humans
* **Model-agnostic**: Applied to any black box model
* **Explanations**: A statement that makes something clear. 


The purpose of lime is to explain the predictions of black box classifiers. What this means is that for any given prediction and any given classifier it is able to determine a small set of features in the original data that has driven the outcome of the prediction.

## ALGORITHM

**1. Permute Data: ** It take observations and create fake data for it. It permuted in different ways.

**2. Calculate distance between permutations and original observations: ** Then it calculate the distance metric and similarity score those fake data and original one.

**3. Make predictions on new data using complex: ** Then it take black box algorithm and make prediction on that dataset.

**4. Pick m features best describing the complex model outcome from the permuted data: ** Then it tries different combinations of predictors ie. m number to figure out minimum number of predictor you have that gives you maximum likelihood of the class that was predicted by the black box.

**5. Fit a simple model to the permuted data with m features and similarity scores as weights: ** Finally it picks those M features and similarity scores and fits the simple model ie. linear model.

**6. Feature weights from the simple model make explanations for the complex models local behaviour: ** The coefficient will serve as an explanation.
