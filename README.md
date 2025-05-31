# Employee Turnover Analysis & Prediction

## 📊 EDA Phase

The EDA explores several factors that might influence whether an employee leaves the company:

- 📉 **Satisfaction Level**: The average satisfaction level is calculated for employees who left and those who stayed, revealing a difference between the two groups.
- 🎯 **Promotion in Last 5 Years**: The code examines the relationship between promotions and retention, showing a higher retention rate among employees who received a promotion.
- 💰 **Salary**: A cross-tabulation and bar plot are used to visualize the relationship between salary levels and employee retention, indicating that salary is a factor, particularly for high earners.
- 🏢 **Department**: A cross-tabulation and bar plot explore the relationship between department and retention.

---

## 🏗️ Model Building Phase

### 🛠️ Feature Engineering

- 🔁 The `salary` column, which is categorical, is converted into numerical format using one-hot encoding. This creates new binary columns (`salary_high`, `salary_low`, `salary_medium`) representing each salary level.
- 🧹 The original `salary` column is dropped from the dataset.

### 📌 Feature Selection

The features selected for the model are:

- `satisfaction_level`
- `average_montly_hours`
- `promotion_last_5years`
- `salary_high`
- `salary_low`
- `salary_medium`

### 🎯 Target Variable

- 🎯 The target variable is the `left` column, which indicates whether an employee left (`1`) or stayed (`0`).

### ✂️ Data Splitting

- 📦 The data is split into training and testing sets using `train_test_split` with a test size of 20%. This ensures that the model is trained on a portion of the data and evaluated on unseen data.

---

## 🤖 Model Training

- A `LogisticRegression` model from the `sklearn.linear_model` library is initialized.
- 🧠 The model is trained using the `fit()` method on the training data (`x_train` and `y_train`). Logistic regression is a statistical model used for binary classification problems. In the training phase, the model learns the relationship between the selected features and the target variable (whether an employee left or not) by adjusting its internal parameters.

---

## ✅ Conclusion

- The code effectively performs EDA to identify potential factors influencing employee turnover.
- 📈 It then builds a logistic regression model using a selected set of features, including numerical and one-hot encoded categorical variables.
- 🔀 The data is split into training and testing sets, and the model is trained on the training data.
- 🔍 The trained model can then be used to predict whether an employee is likely to leave based on their characteristics.
