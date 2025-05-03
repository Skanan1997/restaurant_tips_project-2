# restaurant_tips_project-2

---

**Restaurant Tips Prediction Excel Project**

### Project Overview

**Project Title:** Restaurant Tips Prediction

**Level:** Intermediate

**Tool:** Microsoft Excel (with Data Analysis Add-in)

**Dataset:** Restaurant Tips Dataset.xlsx

This project focuses on building a simple predictive model in Excel to estimate restaurant tips based on customer and billing information. The goal is to understand how different factors (like total bill, party size, and time of day) affect the tip amount and create a linear regression model using Excel. This project is ideal for beginners who want to explore predictive analytics using Excel without coding.

---

### Objectives

* Clean and prepare the dataset for predictive modeling.
* Identify dependent and independent variables.
* Encode categorical variables into numeric form.
* Build a regression model to predict tip amounts.
* Calculate predicted values and evaluate the model using RMSE.
* Derive a mathematical equation for tip prediction.

---

### Project Structure

#### 1. Data Understanding & Setup

**Dataset Features:**

* `sex`: Gender of the customer
* `smoker`: Indicates if the customer is a smoker
* `day`: Day of the restaurant visit
* `time`: Lunch or dinner
* `size`: Number of people dining
* `total_bill`: Total bill amount in USD
* `tip`: Tip amount in USD

**Goal:** Predict the `tip` amount based on various inputs like `total_bill`, `size`, and other features.

---

#### 2. Data Cleaning & Preparation

* **Missing Values Check:**
  Use filters or `COUNTIF` to identify and remove any missing/null values.

* **Feature Identification:**

  * **Independent Variables:** total\_bill, size, sex, smoker, day, time
  * **Dependent Variable:** tip

* **Encoding Categorical Variables:**
  Use `IF` formulas to convert categories to numeric:

  ```excel
  =IF(sex="Male", 1, 0)
  =IF(smoker="Yes", 1, 0)
  =IF(time="Dinner", 1, 0)
  =IF(day="Sun", 1, IF(day="Sat", 2, IF(day="Fri", 3, 4))) 'example
  ```

* Organize the encoded data in a separate worksheet or section for modeling.

---

#### 3. Predictive Modeling

* **Regression Model:**
  Use Excel’s **Data Analysis Toolpak > Regression** tool to build a linear regression model:

  * **Input Y Range:** tip
  * **Input X Range:** total\_bill, size, encoded variables (sex, smoker, time, day)
  * Check the boxes for **Labels** and **Confidence Level** if needed.

* **Prediction Formula:**
  Use the regression output coefficients to write a linear equation:

  ```
  Predicted Tip = β0 + β1*(total_bill) + β2*(size) + β3*(sex_encoded) + ...
  ```

* **Predicted Tip Column:**
  Apply the formula across the sheet to generate predicted values.

* **Error & RMSE Calculation:**

  * Calculate **Error = Actual Tip - Predicted Tip**
  * Calculate **Squared Error**
  * Use:

    ```
    RMSE = SQRT(AVERAGE(Squared Error))
    ```

---

### Findings

* Determine how strongly each factor (like total bill or size) influences the tip amount.
* Identify if smoker status or time of day impacts tipping behavior.
* Evaluate the accuracy of the model using RMSE.

---

### Reports

* **Tip Prediction Report:**
  Summary of actual vs predicted tips with RMSE.

* **Regression Summary:**
  Detailed regression output with coefficients and R² value.

* **Insights Report:**
  Analysis of which factors influence tips the most.

---

### Conclusion

This project demonstrates how predictive modeling can be done in Excel using a simple linear regression approach. It covers data cleaning, feature encoding, model building, prediction, and error evaluation. The final deliverable is a working prediction model that estimates tips based on input variables, complete with a mathematical equation and RMSE validation.

---
## Author - Kanan Sangeet**

This project is part of my analytics portfolio and highlights my ability to build data-driven prediction models using Excel. For questions or collaboration, feel free to connect!

---

