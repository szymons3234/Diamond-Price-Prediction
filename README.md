# Diamond Price Prediction

The aim of this project is to predict the price of diamonds based on their characteristics. The analysis uses the **Diamonds dataset** from Kaggle, which contains **50,000 observations and 10 variables**.
![image](https://github.com/user-attachments/assets/7cca4e94-ce35-49fb-8e51-6f49a2bf59ba)

## Dataset Overview

The dataset includes the following features:

- **carat**: Weight of the diamond.
- **cut**: Quality of the diamond cut (Ideal, Premium, Very Good, etc.).
- **color**: Diamond color grading (D to J).
- **clarity**: Clarity of the diamond (I1 to IF).
- **depth**: Total depth percentage.
- **table**: Width of the diamond's table as a percentage of its diameter.
- **price**: Price in US dollars.
- **x, y, z**: Physical dimensions of the diamond (in mm).

## Key Steps in the Analysis

### 1. Exploratory Data Analysis (EDA)
- Examined the distribution of numeric variables like **carat**, **price**, and **dimensions (x, y, z)**.
- Visualized categorical variables such as **cut**, **color**, and **clarity** using bar plots and pie charts.
- Explored relationships between price and other features using bar plots and scatter plots.

### 2. Data Preprocessing
- Mapped categorical variables (**cut, color, clarity**) to numerical values for analysis.
- Handled outliers and ensured data integrity by analyzing correlations and removing unrealistic values.

### 3. Correlation Analysis
- Heatmap visualization to show correlations between variables, highlighting strong relationships such as between **carat** and **price**.

### 4. Model Building
Three machine learning models were used to predict diamond prices:
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **Linear Regression**

### 5. Model Evaluation
The models were evaluated using metrics such as:
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Error (MAE)**
- **R² Score**

## Results

| Model                  | R² Score | RMSE        | MAE        |
|------------------------|----------|-------------|------------|
| Decision Tree Regressor | 0.964    | 749.26      | 359.30     |
| Random Forest Regressor | 0.982    | 527.17      | 263.07     |
| Linear Regression       | 0.909    | 1186.48     | 786.32     |

The **Random Forest Regressor** achieved the best performance, with the highest accuracy and lowest error metrics. 

### Observations
- Diamonds with **higher carat weight** generally have higher prices.
- However, some diamonds with low carat weights had high prices, likely due to premium qualities in **cut, clarity, and color**.
- Anomalies were observed where diamonds with **J color and I1 clarity** had higher prices than expected, which could be due to unobserved features or market demand.

## Conclusion

The **Random Forest Regressor** outperformed other models and is recommended for diamond price prediction tasks. The analysis also highlighted interesting trends in the dataset, such as unexpected pricing patterns for certain clarity and color grades.

## Technologies Used
- **Python Libraries**: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn
- **Tools**: Jupyter Notebook, Kaggle

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repository/diamond-price-prediction
   cd diamond-price-prediction
