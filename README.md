# RandomForestRegressor_HousingPricesDataset

A Random Forest regression model to predict housing prices from this [dataset](https://www.kaggle.com/datasets/yasserh/housing-prices-dataset).

---

## Dataset Overview

The dataset contains **545 samples** and **13 features**, including:

- **price**
- **area**
- **bedrooms**
- **bathrooms**
- **stories**
- **mainroad**
- **guestroom**
- **basement**
- **hotwaterheating**
- **airconditioning**
- **parking**
- **prefarea**
- **furnishingstatus**

### Sample Rows

| price     | area | bedrooms | bathrooms | stories | mainroad | guestroom | basement | hotwaterheating | airconditioning | parking | prefarea | furnishingstatus  |
|-----------|------|----------|-----------|---------|----------|-----------|----------|-----------------|-----------------|---------|----------|-----------------|
| 13300000  | 7420 | 4        | 2         | 3       | yes      | no        | no       | no              | yes             | 2       | yes      | furnished       |
| 12250000  | 8960 | 4        | 4         | 4       | yes      | no        | no       | no              | yes             | 3       | no       | furnished       |
| 12250000  | 9960 | 3        | 2         | 2       | yes      | no        | yes      | no              | no              | 2       | yes      | semi-furnished  |
| 12215000  | 7500 | 4        | 2         | 2       | yes      | no        | yes      | no              | yes             | 3       | yes      | furnished       |
| 11410000  | 7420 | 4        | 1         | 2       | yes      | yes       | yes      | no              | yes             | 2       | no       | furnished       |

### Dataset Summary

|       | price        | area       | bedrooms | bathrooms | stories | parking |
|-------|-------------|-----------|----------|-----------|---------|---------|
| count | 545         | 545       | 545      | 545       | 545     | 545     |
| mean  | 4,766,729   | 5,150.54  | 2.97     | 1.29      | 1.81    | 0.69    |
| std   | 1,870,440   | 2,170.14  | 0.74     | 0.50      | 0.87    | 0.86    |
| min   | 1,750,000   | 1,650     | 1        | 1         | 1       | 0       |
| 25%   | 3,430,000   | 3,600     | 2        | 1         | 1       | 0       |
| 50%   | 4,340,000   | 4,600     | 3        | 1         | 2       | 0       |
| 75%   | 5,740,000   | 6,360     | 3        | 2         | 2       | 1       |
| max   | 13,300,000  | 16,200    | 6        | 4         | 4       | 3       |

---

## Notebook Structure

The notebook follows these steps:

1. Import libraries
2. Load the dataset
3. Data preprocessing and transformation
4. Compare original vs. transformed dataset
5. Split data into training and test sets
6. Hyperparameter tuning using `GridSearchCV`
7. Display the best hyperparameters
8. Define and train the Random Forest model
9. Evaluate the model
10. Visualize a single Decision Tree from the Random Forest

---

## Model Evaluation

The `RandomForestRegressor` explains approximately **61% of the variance** in housing prices, capturing the main patterns but missing some data complexity.  

- **Mean Absolute Error:** ~940,000 (~20% of the mean price)  
- **R² Score:** 0.61  

This indicates that the model is useful for rough price estimates but not highly precise predictions.

---

Build and trained on [Kaggle](https://www.kaggle.com) by Piyush Nagpal.
