# 🚗 Car Price Prediction Model (Updated for `dataset.csv`)

This project builds and evaluates a machine learning model to predict **car prices** using features such as make, model, year, engine type, mileage, and drivetrain.
It uses **Linear Regression** and **Lasso Regression** models for price prediction, enhanced with automatic data preprocessing and feature encoding.

---

## 📂 Project Files

| File                         | Description                                                                                   |
| ---------------------------- | --------------------------------------------------------------------------------------------- |
| `car prediction model.ipynb` | Original Jupyter/Colab notebook.                                                              |
| `dataset.csv`                | Updated car dataset used for training and testing.                                            |
| `predicted_prices.csv`       | Output file containing actual vs predicted car prices (generated after running the notebook). |
| `README.md`                  | Project documentation and usage instructions.                                                 |

---

## ⚙️ Requirements

This project runs directly in **Google Colab** or any Python 3 environment.

**Libraries Used**

* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `scikit-learn`

You can install the dependencies locally using:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## 🧠 Workflow Overview

1. **Data Loading**

   * Reads the new dataset (`dataset.csv`) containing 1,000+ car records.
2. **Data Cleaning**

   * Drops unused columns (`name`, `description`).
   * Removes rows missing the target (`price`).
   * Fills missing numeric values with median and categorical values with `"Unknown"`.
3. **Feature Engineering**

   * Automatically detects numerical and categorical columns.
   * Encodes categorical features using `OneHotEncoder`.
   * Standardizes numerical features with `StandardScaler`.
4. **Model Training**

   * Trains two regression models:

     * Linear Regression
     * Lasso Regression (for regularization)
5. **Evaluation**

   * Evaluates using **R²**, **MAE**, and **RMSE**.
   * Visualizes actual vs. predicted prices.
6. **Output**

   * Saves predictions as `predicted_prices.csv`.

---

## 🚀 How to Run

### Option 1: In Google Colab

1. Upload `dataset.csv` to your Colab session.
2. Copy and paste the full notebook code (from the provided script) into a Colab cell.
3. Run all cells from top to bottom.
4. The notebook will:

   * Load and preprocess the dataset.
   * Train Linear and Lasso regression models.
   * Display performance metrics and graphs.
   * Save predictions to `predicted_prices.csv`.

### Option 2: Locally

1. Place `dataset.csv` and the notebook in the same directory.
2. Run the notebook using Jupyter Notebook or VS Code.
3. The outputs will be generated in the same folder.

---

## 📈 Evaluation Metrics

| Metric       | Description                                                                  |
| ------------ | ---------------------------------------------------------------------------- |
| **R² Score** | Measures how well the model explains variance in car prices.                 |
| **MAE**      | Mean Absolute Error — average deviation between actual and predicted prices. |
| **RMSE**     | Root Mean Squared Error — penalizes larger prediction errors.                |

---

## 🧾 Notes

* The dataset includes both categorical (make, model, fuel, drivetrain) and numerical (year, mileage, cylinders) variables.
* For best results, ensure your dataset is clean and structured similarly to `dataset.csv`.
* The preprocessing pipeline automatically adjusts to new categories or missing values.

---

## 🧑‍💻 Author

Developed and adapted by Amit Singh using Python and Scikit-learn.
