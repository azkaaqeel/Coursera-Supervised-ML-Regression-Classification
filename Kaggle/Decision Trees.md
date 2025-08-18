
```
    from sklearn.tree import DecisionTreeClassifier

dt_model = DecisionTreeClassifier(
    criterion='gini',
    splitter='best',
    max_depth=5,
    min_samples_split=4,
    min_samples_leaf=2,
    max_features='sqrt',
    random_state=42
)

```

### Pros vs. Cons of Decision Trees

| **Pros**                           | **Cons**                       |
| ---------------------------------- | ------------------------------ |
| Interpretable                      | Prone to Overfitting           |
| Handles Non-Linear Relationships   | High Variance                  |
| Minimal Preprocessing              | Biased on Imbalanced Data      |
| No Assumption of Data Distribution | Poor with Linear Relationships |
| Works on Mixed Data Types          | Suboptimal Greedy Splitting    |
