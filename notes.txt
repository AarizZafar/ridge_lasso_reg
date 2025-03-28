# Ridge vs. Lasso Regression

This section provides an overview of **Ridge Regression** and **Lasso Regression**, two regularization techniques used to enhance linear regression models by adding penalty terms to shrink coefficients.

## Comparison Table

| **Ridge Regression**                                                                                 | **Lasso Regression**                                                                                  |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------|
| Also known as **Tikhonov Regularization**                                                            | Also known as **Least Absolute Shrinkage and Selection Operator**                                     |
| Uses **L2 regularization**: Adds the sum of squared coefficients multiplied by a tuning parameter (λ) | Uses **L1 regularization**: Adds the sum of absolute coefficients multiplied by a tuning parameter (λ) |
| Shrinks coefficients toward zero but never exactly to zero                                           | Can shrink some coefficients exactly to zero, performing feature selection                           |
| Retains all features in the model, reducing the impact of less important ones                        | Produces a sparse model by eliminating less relevant features                                        |
| Discourages large coefficient values, pushing them closer to zero                                    | Drives some coefficients to zero when λ is large enough, simplifying the model                       |
| Useful when you want to keep all variables but minimize the impact of less important features         | Ideal for feature selection, resulting in a simpler model with fewer variables                       |
| Less sensitive to outliers compared to Lasso                                                         | More sensitive to outliers                                                                           |
| Works well with highly correlated features                                                          | Selects one feature from a group of highly correlated ones, setting others to zero                   |
| Does not yield a sparse model (all coefficients remain non-zero)                                     | Yields a sparse model by setting some coefficients to exactly zero                                   |

## Detailed Explanation

### Ridge Regression
- **Purpose**: Introduces a penalty term to prevent overfitting by shrinking coefficient values.
- **Mechanism**: Utilizes L2 regularization, which penalizes the sum of squared coefficients.
- **Effect**: Reduces the magnitude of coefficients, especially for less important features, but never eliminates them entirely.
- **Use Case**: Best when you want to retain all features while minimizing the influence of less significant ones.
- **Advantages**:
  - Handles multicollinearity (highly correlated features) effectively.
  - More robust to outliers compared to Lasso.

### Lasso Regression
- **Purpose**: Adds a penalty term for regularization and performs automatic feature selection.
- **Mechanism**: Employs L1 regularization, summing the absolute values of coefficients.
- **Effect**: Can set coefficients of less important features to exactly zero, resulting in a sparse model.
- **Use Case**: Ideal when the goal is to simplify the model by selecting only the most relevant features.
- **Advantages**:
  - Produces simpler, interpretable models by excluding irrelevant variables.
- **Trade-offs**:
  - More sensitive to outliers.
  - Arbitrarily selects one feature from a group of correlated ones, reducing others to zero.

---

This comparison highlights the key differences between Ridge and Lasso regression, helping you choose the right technique based on your modeling goals.