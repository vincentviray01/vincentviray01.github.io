# Poisoning Attacks and Defenses on Artificial Intelligence: A Survey

## Introduction
Machine learning models are susceptible to a variety of attacks during both training and inference. 

This research paper focuses on attacks during training, particularly the data poisoning attac, and several defenses against it.

This is an attack that "poisons" data during the training phase and therefore reduces the model's accuracy during inference.

There are two types of attacks:
1. Attacks on Non-Neural Networks
2. Attacks on Neural Networks

## Knowledge Background
### Manipulations
Techniques
1. Modification of data labels
2. Injections of malicious samples
3. Manipulation of the training data

The damage done by these techniques will show up during model inference where the accuracy of the model will be significantly reduced.

Some forms of manipulating training data include:
1. Altering images without changing the label
2. Adding inputs that causes a classifier to learn to make the wrong predictions

There are two goals for adversarial attacks:
1. A targeted attack where adversarial examples are included in the training data that causes the model to misclassify the data into a specific class
2. A non-targeted attack where the adversarial examples causes the model to misclassify in general and not to a specific class

Note: Evasion attacks are another type of training data manipulation, but they do not require knowledge of training data

### Assumptions of Attack and Defense
Attacks on machine learning models falls into two categories:
1. Data poisoning (DP) attacks, which are applied during training
2. Adversarial attacks, which are applied during testing

   ![image](https://github.com/vincentviray01/vincentviray01.github.io/assets/47910310/42297ec6-34c1-4ec1-8823-7e7701de132a)
[^1]


Citations:

[1] https://arxiv.org/pdf/2202.10276.pdf
