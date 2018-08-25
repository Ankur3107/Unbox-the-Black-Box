# Unbox-the-Black-Box

# OBJECTIVE

Actually I was thinking about ‘how to get the machine learning model explantion’. Then I searched on Google and found a great package called LIME by Tulio Ribeiro, Sameer Singh and Carlos Guestrin. I was very impressed with the package. In this kernel, I will share my knowledge that i got from different papers, blogs and videos.

# LIME : Locally Interpretable Model-agnostic Explanations


<center><iframe width="560" height="315" src="https://www.youtube.com/embed/hUnRCxnydCc" frameborder="0" allowfullscreen></iframe></center>


## ABSTRACT

Machine learning models remain mostly black boxes. Understanding the reasons behind predictions is, however, quite important in assessing trust, which is fundamental if one plans to take action based on a prediction, or when choosing whether to deploy a new model. Such understanding also provides insights into the model, which can be used to transform an untrustworthy model or prediction into a trustworthy one.

## WHAT IS LIME

* **Locally**: Locally faithful to the classifier
* **Interpretable**: Representation that is understandable to humans
* **Model-agnostic**: Applied to any black box model
* **Explanations**: A statement that makes something clear. 


The purpose of lime is to explain the predictions of black box classifiers. What this means is that for any given prediction and any given classifier it is able to determine a small set of features in the original data that has driven the outcome of the prediction.
