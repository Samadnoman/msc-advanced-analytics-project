# MSc Advanced Analytics Project: Classification and Regression in R

A two-part supervised machine learning project in R, completed for the Advanced Analytics module of my MSc in Data Analytics (2026). Part 1 predicts a category and Part 2 predicts a number. Each part follows the same workflow: data preparation, exploratory analysis, modelling, tuning, diagnostics and evaluation on unseen test data.

The two parts sit in separate folders because the module required separate classification and regression files.

## Project at a glance

| | [Part 1: Classification](classification/) | [Part 2: Regression](regression/) |
|---|---|---|
| **Question** | Is a breast tumour benign or malignant? | What drives house price per unit area? |
| **Data** | Breast Cancer Wisconsin (683 samples after cleaning) | Real Estate Valuation (414 transactions) |
| **Models** | Decision Tree and kNN, tuned with 10-fold cross-validation | Multiple linear regression, full vs reduced model |
| **Best result** | kNN: 97.55% test accuracy, 97.18% sensitivity | Test RMSE 7.18, MAE 5.60, MAPE 15.3% |
| **Report** | [View HTML report](https://samadnoman.github.io/msc-advanced-analytics-project/classification/breast_cancer_classification.html) | [View HTML report](https://samadnoman.github.io/msc-advanced-analytics-project/regression/real_estate_regression.html) |

## Key insights

- **Classification:** three cell measurements are enough for a readable Decision Tree with 97% accuracy. kNN does slightly better, and both models missed only 2 of 71 malignant tumours.
- **Regression:** distance to public transport is the strongest driver of house prices. Each extra 100 m from a metro station is linked to a lower price, while nearby shops are linked to a higher one.

## Skills shown

- **Data preparation:** handling missing values, recoding variables, stratified and random train/test splits
- **Exploratory analysis:** summary statistics, boxplots, scatter plots and correlation analysis
- **Classification:** Decision Tree (`rpart`) and kNN with hyperparameter tuning in `caret`
- **Classification evaluation:** confusion matrix, sensitivity, specificity, precision, F1-score and balanced accuracy
- **Regression:** coefficient interpretation, VIF, Shapiro-Wilk, Breusch-Pagan and Cook's distance
- **Regression evaluation:** RMSE, MAE, MAPE and AIC-based model comparison
- **Reporting:** reproducible R Markdown reports

## Repository structure

```
classification/   Breast cancer classification: R Markdown, HTML report, data, plots
regression/       Real estate price regression: R Markdown, HTML report, data, plots
```

## Tools

R, R Markdown, caret, rpart, rpart.plot, readxl, car, lmtest

## Data sources

Both datasets come from the UCI Machine Learning Repository: [Breast Cancer Wisconsin (Original)](https://archive.ics.uci.edu/dataset/15/breast) and [Real Estate Valuation](https://archive.ics.uci.edu/dataset/477/real+estate+valuation+data+set).

## Licence

Code is released under the [MIT Licence](LICENSE). The datasets keep their original UCI terms.
