# Elevate Labs Internship: Task 3

## Task 3: Linear Regression on Housing Dataset

This section contains the deliverables for Task 3, focusing on implementing and understanding simple and multiple linear regression to predict house `price` using the `Housing.csv` dataset.

### Files (Task 3)

- **Notebook**:
  - `ElevateLabsTask-3.ipynb`: Jupyter Notebook containing the linear regression code, including data preprocessing, model fitting, evaluation, and visualization.

- **Data**:
  - `Housing.csv`: House price dataset (545 rows, 13 columns: `price`, `area`, `bedrooms`, `bathrooms`, `stories`, `mainroad`, `guestroom`, `basement`, `hotwaterheating`, `airconditioning`, `parking`, `prefarea`, `furnishingstatus`).

- **Visualizations**:
  - `predicted_vs_actual.png`: Predicted vs. actual `price` for multiple linear regression. Visualizes model performance (points closer to the diagonal indicate better predictions).
  - `simple_regression_line.png`: Regression line for simple linear regression (`area` → `price`). Shows a positive relationship (larger area, higher price).

- **Additional Files**:
  - `task 3.pdf`: PDF document (contents not specified, assumed to be a report or supplementary material for Task 3).

### Approach (Task 3)
- **Preprocessing**: Encoded categorical variables (`mainroad`, `guestroom`, etc.) as 1/0 (yes/no) and `furnishingstatus` as 0 (furnished), 1 (semi-furnished), 2 (unfurnished).
- **Simple Linear Regression**: Used `area` to predict `price`, showing a positive relationship (larger area increases price). Evaluated with MAE, MSE, and R².
- **Multiple Linear Regression**: Used all features to predict `price`. Improved R² compared to simple regression, with coefficients showing feature impacts (e.g., `airconditioning` increases price, `furnishingstatus=unfurnished` decreases price).
- **Evaluation Metrics**: MAE, MSE, and R² are printed in the notebook (Cells 4 and 6). MAE is preferred due to potential price outliers, though MSE penalizes larger errors more heavily.
- **Interpretation**: Coefficients are interpreted in the notebook output (e.g., a positive `area` coefficient confirms larger houses cost more). Plots visualize relationships and model fit.
- **Multicollinearity Check**: VIF analysis is included to detect multicollinearity (e.g., `bedrooms` and `stories` may be correlated).

### Notes for Mentors (Task 3)
- `price` was chosen as the target for regression as it’s continuous and fits the house price prediction example in the task.
- Multicollinearity may exist between features like `bedrooms` and `stories` (checked via VIF). This could affect coefficient stability but doesn’t impact predictions.
- All steps (preprocessing, model fitting, evaluation, visualization) are in `ElevateLabsTask-3.ipynb`, with cells numbered and commented for clarity.
- The `task 3.pdf` file is included as per the directory listing; its contents are assumed to be a report or additional documentation.

### How to View (Task 3)
- Open `ElevateLabsTask-3.ipynb` in Jupyter Notebook to see the code, evaluation metrics, coefficient interpretations, and VIF analysis.
- View PNG files (`predicted_vs_actual.png`, `simple_regression_line.png`) in any image viewer to visualize the regression results.
- Open `task 3.pdf` in a PDF viewer to review any additional documentation or report.
- Ensure `Housing.csv` is in the same directory as the notebook to run the code successfully.
