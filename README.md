# Monthly Budgeting & Forecasting Model in Excel

## 🎯 Overview

This repository contains a comprehensive, dynamic Excel model for **monthly budgeting and financial forecasting**. Designed for analysts and business users, this model allows for scenario planning by linking historical data to future projections, ultimately generating a full, dynamic Profit and Loss (P&L) statement.

The model uses Excel's robust financial and logic functions to create a system where users can instantly switch between different operating scenarios (Best, Base, Worst Case) to assess their impact on profitability.

***

## 📊 Key Features & Functionality

The model is built around three core components:

### 1. Actuals & Forecasting

* **Historical Data:** Links actual historical operating expenses by department.
* **Time Series Forecasting:** Uses the `FORECAST.ETS` function to project future monthly operating expenses, weighing recent data more heavily and accounting for trends.
* **Dynamic Assumptions:** Assumptions for Best and Worst Case scenarios are linked to percentages (e.g., +/- 30% from the Base Case), making the model highly flexible.

### 2. Scenario Management (Live Case)

* **Scenario Selection:** A central "Live Case" section allows the user to select one of the three scenarios (1 for Best, 2 for Base, 3 for Worst).
* **`CHOOSE` Function:** The `CHOOSE` function is used to dynamically pull the corresponding forecast data into the Live Case, instantly updating the entire P&L statement based on the selection.
* **Data Validation:** Implements data validation to ensure the user can only select a valid scenario number (1, 2, or 3).

### 3. Dynamic Profit and Loss (P&L) Statement

* **Expense Aggregation:** The `SUMIFS` function is used to aggregate the Live Case forecasted expenses into P&L line items (e.g., summing all Marketing expenses).
* **Revenue Modeling:** Revenue is calculated based on assumptions for Customer Acquisition Cost (CAC) and Price, linked to the forecasted Marketing spend.
* **Logic for Taxes:** An `IF` statement is used to ensure taxes are only applied when there is a positive Pre-Tax Income.
* **Financial Output:** Calculates Gross Profit, Operating Income, and Net Income, which update automatically when the scenario is changed.

***

## 🛠 Prerequisites

* **Microsoft Excel:** You must have a version of Microsoft Excel (2016 or later) to use the advanced forecasting functions.
* **Financial Modeling Basics:** Familiarity with P&L structure (Income Statement) is recommended.

***

## 🚀 How to Use the Files

1.  **Download:** Clone the repository or download the `Budgeting_Forecasting_Model.xlsx` file.
2.  **Explore the Forecast Sheet:** Examine how the `FORECAST.ETS` function is applied across different expense lines.
3.  **Test Scenarios:** Navigate to the P&L sheet and change the "Operating Scenario" number (1, 2, or 3) to see the immediate impact on the final **Net Income**.
4.  **Modify Assumptions:** Change the percentage assumptions for the Best/Worst cases to customize the model to your specific needs.
