# Exploratory Data Analysis (EDA) Report

## 📘 Project Overview


## 📂 Dataset

The project uses two main datasets:

* **`train.csv`** – Primary dataset used for exploration and analysis.
* **`test.csv`** – Dataset intended for model evaluation or submission generation.

---

## 🧩 Key Objectives

* Understand the data structure, size, and missing patterns.
* Explore distributions of numerical and categorical variables.
* Identify correlations and outliers.
* Visualize relationships between input features and target variable (*e.g., Delivery_Lag*).
* Prepare clean, feature-rich data for predictive modeling.

---

## 🔍 Data Inspection

* Loaded using **pandas** and previewed via `head()` and `info()`.
* Checked data types, null values, and duplicates.
* Verified target column distribution (`Delivery_Lag`).

---

## 📊 Visual Explorations

A variety of plots were used to understand data behavior:

| Visualization                    | Purpose                                                     |
| -------------------------------- | ----------------------------------------------------------- |
| **Histogram & KDE**              | Examine numeric distributions and skewness.                 |
| **Boxplot**                      | Detect outliers and compare across categories.              |
| **Countplot**                    | Show class frequencies for categorical features.            |
| **Heatmap (Correlation Matrix)** | Identify multicollinearity and strong linear relationships. |
| **Pairplot / Scatterplot**       | Explore inter-variable relationships visually.              |

Example: Distribution of `Delivery_Lag` to identify typical delivery times and extreme cases.

---

## ⚙️ Preprocessing & Cleaning

* Handled **missing values** using `SimpleImputer` / manual replacement where necessary.
* Standardized categorical column names.
* Encoded categorical variables for later use in ML pipelines.
* Detected and treated outliers using IQR / z-score methods.
* Applied **scaling or transformation** to normalize skewed numerical variables.

---

## 📈 Feature Engineering

Derived new or composite features such as:

* Time-based or lag-related metrics (`Delivery_Lag`)
* Ratios and differences between numeric variables
* Aggregated statistics (mean, median, etc.) for group-based insights

---

## 💡 Insights Summary

Some notable findings (based on code review):

* Delivery times exhibit moderate skewness, suggesting a log transformation might help.
* Certain categorical variables show strong class imbalance.
* Several numerical variables have high pairwise correlation (>0.8), possibly redundant.
* Feature scaling significantly improves model readiness.

---

## 🧰 Libraries Used

* `numpy`
* `pandas`
* `matplotlib`
* `seaborn`
* `scipy.stats`

---

