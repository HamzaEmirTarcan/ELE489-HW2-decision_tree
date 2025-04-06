# Banknote Authentication using Decision Tree

This project applies a Decision Tree classifier on the Banknote Authentication dataset to distinguish between genuine and fake banknotes based on statistical features extracted from banknote images.
Dataset
- Source: UCI Machine Learning Repository  
- Format: `.txt` (CSV-like structure)
- Features:
  - **variance** of Wavelet Transformed image
  - **skewness**
  - **kurtosis**
  - **entropy**
- Class Label:
  - `0` → Fake
  - `1` → Authentic

What Was Done

- **EDA (Exploratory Data Analysis)** using pairplots to analyze feature-class separability
- **Decision Tree training** with different hyperparameters:
  - `criterion`: `"gini"` vs `"entropy"`
  - `max_depth`: limited and unlimited
  - `min_samples_split`: 2, 5, 10
- **Model evaluation** using:
  - Accuracy
  - Precision, Recall, F1-score (`classification_report`)
  - Confusion Matrix
- **Visualization**:
  - Decision tree plots using `plot_tree()`
  - Feature importance analysis

Summary of Results

| Model | Criterion | Max Depth | Accuracy |
|-------|-----------|-----------|----------|
| A     | entropy   | None      | 99%      |
| B     | entropy   | 3         | 94%      |
| C     | gini      | 3         | 92%      |

- Features `variance` and `kurtosis` were most important.
- `entropy` feature was unused in the final tree (importance = 0.0).
💬 Conclusion

Decision Tree is a highly suitable model for this dataset, offering high performance and clear interpretability. The model benefits from the natural feature separability in the data.
🔗 Files

- `decision_tree_hw2.ipynb`: All code and outputs
- `README.md`: This file
