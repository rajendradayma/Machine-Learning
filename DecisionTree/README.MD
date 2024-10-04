#DECISION TREE
A Decision Tree is a popular machine learning algorithm used for both classification and regression tasks. It creates a model that predicts the value of a target variable by learning simple decision rules inferred from the features of the data. Decision trees are easy to understand and interpret, and they mimic the human decision-making process by splitting the dataset based on feature values.

Key Concepts:
Nodes:

Root Node: The topmost node that represents the entire dataset and gets split into two or more homogenous sets.
Internal Nodes: Nodes that represent a feature or attribute upon which the dataset is split.
Leaf Nodes: Terminal nodes that represent the outcome or class label for classification or predicted value for regression.
Splitting: The process of dividing the dataset into smaller subsets based on feature values. Different splitting criteria are used depending on the problem (e.g., Gini Index, Entropy for classification).

Pruning: The technique of reducing the size of the tree by removing sections that have little importance. This prevents overfitting, where the model becomes too complex and performs well on training data but poorly on new, unseen data.
Types of Decision Trees:
Classification Trees: Used when the target variable is categorical (e.g., predicting if an email is spam or not).
Regression Trees: Used when the target variable is continuous (e.g., predicting house prices).
Insights from Decision Trees:
Interpretability: Decision trees are simple to visualize and explain. The flowchart-like structure helps identify how features influence the prediction.
Feature Importance: By examining the nodes, you can see which features are most important in making predictions.
Non-Linear Boundaries: Decision trees can capture non-linear relationships between the features and the target variable, unlike linear models.
Hyperparameters in Decision Trees:
Criterion:
Gini Impurity: Measures how often a randomly chosen element would be incorrectly labeled. Lower values are better.
Entropy (Information Gain): Measures the disorder or uncertainty in the dataset. Lower entropy implies higher purity after splitting.
Max Depth: The maximum depth of the tree (i.e., the number of splits or layers). Limiting the depth helps avoid overfitting.

High Depth: Can lead to overfitting by making the tree too specific to the training data.
Low Depth: Can lead to underfitting if the model is too simple and cannot capture patterns.
Min Samples Split: The minimum number of samples required to split a node. If this value is too small, the model will overfit; if it’s too large, the model might miss important patterns.

Small Value: The tree becomes deeper, with more splits, increasing the risk of overfitting.
Larger Value: The tree will split only when there is enough data, reducing the risk of overfitting.
Min Samples Leaf: The minimum number of samples required to be at a leaf node. It prevents the model from creating leaves with very few samples, which can help in generalization.

Small Value: Leads to small leaves, increasing complexity and the chance of overfitting.
Large Value: Reduces complexity, which can lead to underfitting.
Max Features: The maximum number of features to consider when looking for the best split. It helps in controlling overfitting.

sqrt(n) or log2(n) for large datasets is common for classification trees.
Max Leaf Nodes: Limits the number of leaf nodes in the tree. A smaller number of leaf nodes can make the model more general and reduce overfitting.

Random State: Controls the randomness involved in certain aspects like the data shuffling before splitting. Setting a fixed seed ensures reproducibility of results.

Advantages:
Easy to interpret and visualize.
Handles both categorical and numerical data.
Non-parametric, so it can model non-linear relationships well.
Disadvantages:
Overfitting: If not pruned, decision trees can become too complex and capture noise in the data.
Bias: Can be sensitive to small changes in data, as a small change might cause the tree structure to shift significantly.
