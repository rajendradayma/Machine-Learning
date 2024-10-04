A Voting Classifier is an ensemble learning method that combines the predictions from multiple different machine learning models to improve overall performance. The idea is that by aggregating the predictions of several models, the final prediction can be more accurate than any single model's prediction.

There are two types of Voting Classifiers:

Hard Voting: The classifier predicts the class label that has been predicted the most frequently by the base classifiers (majority voting).
Soft Voting: The classifier predicts the class label based on the average of predicted probabilities, favoring the classes with higher confidence levels across models.
Concept:
Hard Voting: In this method, each model in the ensemble votes for a class, and the class that gets the majority of votes is the final prediction.
![image](https://www.researchgate.net/publication/351941675/figure/fig7/AS:1028438324441103@1622210212985/An-overview-of-the-voting-ensemble-classifier-built-from-SVM-and-RF-base-models.png)
Example: If three classifiers predict labels as [A, B, A], the Voting Classifier with hard voting will choose A, as it has the majority of votes.

Soft Voting: Here, each classifier outputs the probability of each class, and the class with the highest averaged probability is chosen.

Example: Suppose you have three classifiers, and their predicted probabilities for class A are [0.7, 0.8, 0.6]. The average probability for class A is 0.7, and this averaged value is used to make the prediction.
Hyperparameters of Voting Classifier
1. estimators:
A list of tuples, where each tuple consists of a string name and the classifier object. The list can contain multiple classifiers (e.g., Decision Tree, Logistic Regression, SVM, etc.).

Example: estimators=[('lr', LogisticRegression()), ('svc', SVC()), ('rf', RandomForestClassifier())]
2. voting:
Specifies the voting type. It can be either:
'hard': Uses majority voting for class labels.
'soft': Uses averaged predicted probabilities for voting.
Example: voting='soft'
3. weights (Optional):
A list of weights for each classifier. By default, all classifiers are given equal weight (1). You can assign higher weights to classifiers that you believe are more important.
Example: weights=[2, 1, 3] would give more weight to the first and third classifiers.
4. n_jobs:
Specifies the number of cores to use for parallel processing. If set to -1, all available processors will be used.
Example: n_jobs=-1 (use all cores).
5. flatten_transform (default True):
Used for soft voting. If True, the predicted probabilities from each base classifier will be flattened into a single array.
6. verbose (default False):
If set to True, it prints progress messages during the fitting process. It can be useful to track training in larger ensembles.
Insights:
Bias-Variance Tradeoff: Voting classifiers can reduce overfitting and variance by combining weak or different types of classifiers. This generally improves performance when individual classifiers have different strengths.
Diversity of Models: The models included in the voting classifier should be diverse (e.g., Logistic Regression, Decision Trees, and SVM), so that they complement each other rather than making similar mistakes.
