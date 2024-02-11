# Evaluation Summary of Three Supervised Learning Algorithms for Algorithmic Trading

In algorithmic trading, the choice of supervised learning algorithms is critical for making informed investment decisions. Here, we evaluate the performance of Support Vector Classifier (SVC), Logistic Regression, and AdaBoost Classifier in the context of algorithmic trading. SVC serves as the base model for comparison.

## Support Vector Classifier (SVC):

### Strengths:

- Effective in high-dimensional spaces, making it suitable for feature-rich datasets often encountered in financial markets.
- Robust against overfitting, especially in cases where the number of features exceeds the number of samples.
- Versatile due to various kernel functions available (linear, polynomial, radial basis function), allowing adaptation to different types of data distributions.

### Weaknesses:

- Computationally expensive, especially with large datasets, and may not scale well.
- Sensitive to the choice of hyperparameters, such as the regularization parameter C and the kernel parameters.
- Not inherently capable of handling imbalanced datasets, which is common in financial markets where anomalies are rare but significant.

### Results

![SVM Model Actual Returns vs Strategy Returns](Resources/SVC Chart.png)

![SVM Model Training and Testing Reports](Resources/SVM Reports.png)


## Logistic Regression:

### Comparison against SVC:

#### Strengths:

- Simplicity and interpretability make it easy to understand and implement, providing insights into the relationship between features and the target variable.
- Efficient training and prediction times, suitable for large datasets and real-time trading scenarios.
- Naturally handles binary classification tasks and can be extended to multi-class problems using techniques like one-vs-rest or softmax regression.

#### Weaknesses:

- Assumes a linear relationship between features and the log-odds of the target variable, limiting its ability to capture complex nonlinear patterns.
- Susceptible to outliers and noise, which can affect model performance, particularly when dealing with unclean financial data.
- May struggle with highly correlated features, leading to unstable estimates of coefficients and reduced interpretability.


### Results

![Logistic Regression Model Actual Returns vs Strategy Returns](Resources/Logistic Regression Chart.png)

![Logistic Regression Model Training and Testing Reports](Resources/Logistic Regression Reports.png)

## AdaBoost Classifier:

### Comparison against SVC:

#### Strengths:

- Ensemble learning technique that combines multiple weak learners (typically decision trees) to create a strong learner, effectively capturing complex relationships in the data.
- Automatically handles feature selection by focusing more on informative features through iterative training rounds.
- Less prone to overfitting compared to individual decision trees, thanks to the boosting algorithm's adaptive nature.

#### Weaknesses:

- Sensitive to noisy data and outliers, which can adversely affect the performance of subsequent weak learners.
- Relatively slower training compared to simpler models like logistic regression, especially with a large number of weak learners or complex base classifiers.
- Requires careful tuning of hyperparameters, such as the number of weak learners and the learning rate, to prevent underfitting or overfitting.

### Results

![Adaboost Model Actual Returns vs Strategy Returns](Resources/Adaboost Chart.png)

![Adaboost Regression Model Training and Testing Reports](Resources/Adaboost Reports.png)

## Conclusion:

While SVC offers a robust baseline for algorithmic trading tasks, logistic regression and AdaBoost provide alternative approaches with their simplicity and ensemble-based techniques, respectively. Logistic regression offers transparency and efficiency, while AdaBoost excels in capturing complex patterns and handling feature selection automatically. The choice among these algorithms depends on factors such as dataset characteristics, interpretability requirements, and computational resources available.
