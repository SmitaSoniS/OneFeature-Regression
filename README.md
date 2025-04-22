## WiDS: Agent Jackie Assignment 1 Dataset – Linear Regression and Model Evaluation

This project uses the **WiDS: Agent Jackie Assignment 1 Dataset** from Kaggle to build a linear regression model that predicts a target variable using a single feature. The goal is to explore the relationship between the feature and the target variable, manually implement linear regression using the **Ordinary Least Squares (OLS)** method, check all assumptions of linear regression, and assess the model's performance using key metrics and visualizations.

### **Project Overview**

- **Single Feature Regression**: The project focuses on building a linear regression model using one independent variable (feature) to predict the dependent variable (target).
- **Linear Regression Model**: Implement the linear regression model from scratch using the **OLS method** to calculate the slope (**w**) and intercept (**b**) of the regression line.
- **Model Evaluation**: Evaluate the performance of the model using metrics such as Mean Squared Error (MSE), R-squared (R²), and residual analysis.
- **Assumptions Checking**: Check the assumptions of linear regression, ensuring the model is appropriate for the given data.

### **Features**

- **Target Variable (Dependent Variable)**: The variable that I aim to predict.
- **Independent Variable (Single Feature)**: The single feature used to predict the target variable.

### **Goals**

1. **Explore Feature-Target Relationship**: 
   - Visualize the relationship between the independent variable and the target variable using scatter plots and a regression line.
   
2. **Build a Linear Regression Model Using OLS**:
   - Manually implement a **Linear Regression** model using the **Ordinary Least Squares (OLS)** method to calculate the model parameters:
   
   ```
   y = b + w * x
   ```

   where:
   - y is the target variable,
   - x is the independent variable,
   - b is the intercept, and
   - w is the slope.

3. **Check Assumptions of Linear Regression**:
   - **Linearity**: Check that the relationship between the independent variable and the target variable is linear.
   - **Independence**: Ensure that the residuals (errors) are independent of each other.
   - **Homoscedasticity**: Verify that the residuals have constant variance across all levels of the independent variable.
   - **Normality**: Assess if the residuals are approximately normally distributed.
   
4. **Model Evaluation**:
   - Assess the model's performance using the following metrics:
     - **Mean Squared Error (MSE)**: Measures the average squared difference between predicted and actual values. The formula for MSE is:

       ```
       MSE = (1/n) * Σ(y_i - ŷ_i)²
       ```

       where:
       - y_i is the actual value,
       - ŷ_i is the predicted value, and
       - n is the number of data points.
     
     - **R-squared (R²)**: Represents how well the model explains the variance in the target variable. The formula for R² is:

       ```
       R² = 1 - Σ(y_i - ŷ_i)² / Σ(y_i - ȳ)²
       ```

       where:
       - ȳ is the mean of the actual target variable values.
       
   - Generate residual plots to evaluate the model's error and check if the assumptions of linear regression hold.

### **Dataset Information**

- The **WiDS: Agent Jackie Assignment 1 Dataset** contains a single feature that will be used to predict the target variable.
- The dataset includes numerical values, which are suitable for a regression analysis using the linear regression model.

### **Required Tools**

To run this project, ensure you have the following installed:
- **Python 3.x**
- **Key Libraries**:
  - `pandas` for data manipulation
  - `numpy` for numerical operations
  - `matplotlib` and `seaborn` for data visualization

### **Steps to Complete the Project**

1. **Data Loading and Preprocessing**:
   - Load the dataset and examine the feature-target relationship.
   - Handle any missing values, if necessary, and prepare the data for modeling.

2. **Implementing Linear Regression Using the OLS Method**:
   - **Calculate the slope** (w) and **intercept** (b) using the **Ordinary Least Squares (OLS)** method:
     - **OLS Formula for w (slope)**:

       ```
       w = Σ(x_i - x̄)(y_i - ȳ) / Σ(x_i - x̄)²
       ```

     - **OLS Formula for b (intercept)**:

       ```
       b = ȳ - w * x̄
       ```

     where:
     - x_i and y_i are individual data points,
     - x̄ and ȳ are the means of the independent and dependent variables, respectively.
   
   - Use these values of w and b to make predictions for the target variable.

3. **Check Assumptions of Linear Regression**:
   - **Linearity**: Plot the data points and the regression line to verify that the relationship between the feature and the target variable is linear.
   - **Independence**: Use autocorrelation plots or check the residuals over time (if applicable) to confirm that errors are independent.
   - **Homoscedasticity**: Plot the residuals against the fitted values to check if the variance of residuals is constant.
   - **Normality**: Create a histogram or Q-Q plot of the residuals to check if they follow a normal distribution.

4. **Data Visualization**:
   - Create scatter plots to visualize the relationship between the feature and the target.
   - Overlay the regression line (from the OLS calculation) to see how well the model fits the data.
   - Generate residual plots to further investigate the assumptions.

5. **Model Evaluation**:
   - Calculate the **Mean Squared Error (MSE)** using the formula:

     ```
     MSE = (1/n) * Σ(y_i - ŷ_i)²
     ```

     where y_i is the actual value and ŷ_i is the predicted value.
   - Calculate the **R-squared (R²)** using:

     ```
     R² = 1 - Σ(y_i - ŷ_i)² / Σ(y_i - ȳ)²
     ```

   - Generate **residual plots** to visualize the difference between the observed and predicted values.

6. **Analysis and Conclusion**:
   - Based on the evaluation metrics, analyze how well the linear regression model performed.
   - Interpret the residual plots to check for patterns in model errors and assess if any improvements are needed.
   - Ensure that the assumptions of linear regression are met and suggest any necessary model adjustments.

### **Installation and Setup**

Ensure you have the following libraries installed:

```bash
pip install pandas numpy matplotlib seaborn
```

### **Project Outcomes**

- Developed a simple linear regression model to predict the target variable using a single feature
- Achieved an R-squared value of 0.81, indicating that 81% of the variation in the target variable is explained by the model, demonstrating a strong fit
- The model's Root Mean Squared Error (RMSE) is 0.08, meaning the predictions deviate by just 0.08 units on average, highlighting minimal prediction error
