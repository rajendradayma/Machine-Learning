Hyperparameters for Polynomial Regression:
Polynomial regression has a few key hyperparameters:
![ie](https://builtin.com/sites/www.builtin.com/files/styles/ckeditor_optimize/public/inline-images/polynomial-regression-3.png)

Degree of the Polynomial (degree):

This is the most important hyperparameter.

It determines the complexity of the model. A higher degree captures more complex relationships, but it can also lead to overfitting.

Example: PolynomialFeatures(degree=2) will create a second-degree polynomial (quadratic).

Tuning: You can tune this hyperparameter to achieve a balance between bias and variance. A higher degree might capture the data better but may also overfit.

Interaction Only (interaction_only):
When True, only interaction terms are produced (i.e., terms like 𝑥1× 𝑥2x1 × x2), not power terms like 
𝑥12x12.
Default: False (i.e., the model includes both power and interaction terms).
Include Bias (include_bias):

Whether to include a bias term (an intercept) in the polynomial features.
Default: True.
Regularization Parameters (when using with ridge or lasso regression):

Polynomial regression can lead to overfitting with high-degree polynomials, so you may use ridge or lasso regression to regularize the model.
Ridge (L2 regularization): Controls how much penalty is applied to large coefficients.
Lasso (L1 regularization): Adds penalty for non-zero coefficients, which can help with feature selection by setting some coefficients to zero.
