# Telco Customer Churn Analysis

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Analysis-Pandas-150458?logo=pandas)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange?logo=jupyter)
![Status](https://img.shields.io/badge/Project-Exploratory%20Data%20Analysis-success)

## Project Overview

Customer churn is an important challenge for telecommunications
companies because losing existing customers can affect recurring revenue
and long-term growth. This project explores a telecom customer dataset
to understand customer churn patterns and identify customer groups and
service-related factors associated with customers leaving the company.

The analysis was performed using Python in Jupyter Notebook, with Pandas
for data manipulation and Matplotlib/Seaborn for visual exploration.

## Business Objective

The goal is to answer questions such as:

-   What proportion of customers have churned?
-   Does churn vary by customer tenure or contract type?
-   Are senior citizens more likely to churn?
-   How are internet services, online security, and technical support
    associated with churn?
-   Does the payment method show any relationship with churn?

## Dataset

-   **Dataset:** Telco Customer Churn
-   **Rows:** 7,043 customer records
-   **Columns:** 21
-   **Target variable:** `Churn` (`Yes` / `No`)

The dataset includes customer demographics, account information,
subscribed services, contract details, payment method, monthly charges,
total charges, and churn status.

## Tools & Technologies

-   **Python**
-   **Pandas** -- data loading, cleaning, transformation, and
    aggregation
-   **NumPy** -- numerical operations
-   **Matplotlib** -- charts and visualizations
-   **Seaborn** -- statistical data visualization
-   **Jupyter Notebook** -- analysis environment

## Project Workflow

1.  Loaded the customer churn dataset into a Pandas DataFrame.
2.  Reviewed the dataset structure, data types, and descriptive
    statistics.
3.  Converted blank values in `TotalCharges` to `0` and changed the
    column to a numeric data type.
4.  Checked for missing values and duplicate customer IDs.
5.  Converted `SeniorCitizen` values from `0`/`1` to readable `no`/`yes`
    labels.
6.  Performed exploratory data analysis (EDA) using count plots, a pie
    chart, a histogram, and a percentage-stacked bar chart.
7.  Compared churn patterns across demographic groups, tenure,
    contracts, subscribed services, and payment methods.

## Key Results

### Overall churn

  Customer status     Customers    Percentage
  ----------------- ----------- -------------
  Churned (`Yes`)         1,869    **26.54%**
  Retained (`No`)         5,174    **73.46%**
  **Total**           **7,043**   **100.00%**

Approximately **1 in 4 customers** in the dataset churned. The remaining
73.46% stayed with the company.

### Data quality checks

  Check                             Result
  ------------------------------- --------
  Customer records                   7,043
  Features / columns                    21
  Missing values after cleaning          0
  Duplicate customer IDs                 0

### Descriptive statistics

  Metric                  Mean     Median   Minimum    Maximum
  ----------------- ---------- ---------- --------- ----------
  Tenure (months)        32.37         29         0         72
  Monthly charges        64.76      70.35     18.25     118.75
  Total charges       2,279.73   1,394.55      0.00   8,684.80

*Charge values are shown in the units provided by the source dataset.*

## Insights from Exploratory Analysis

The following are the patterns observed in the notebook's visual
analysis:

1.  **Tenure:** Customers with longer service tenure appear more likely
    to remain customers. Churn is more concentrated among customers with
    very short tenure, particularly around the first few months.
2.  **Contract type:** Month-to-month customers show substantially more
    churn than customers on one-year or two-year contracts.
3.  **Senior citizens:** The percentage-stacked comparison indicates a
    higher churn proportion among senior citizens than non-senior
    citizens.
4.  **Online security and technical support:** Customers without Online
    Security and Tech Support show higher churn in the visual
    comparisons than customers who have these services.
5.  **Internet service:** Fiber optic customers form a notable group
    among churned customers in the count plots. A count comparison
    should not be interpreted as a churn rate unless each category is
    divided by its own customer total.
6.  **Payment method:** Electronic check users show a comparatively high
    number of churned customers in the payment-method chart.

> **Percentage interpretation:** The overall churn percentages above are
> calculated from the dataset totals recorded in the analysis. The
> notebook currently contains charts and qualitative observations for
> the customer segments, but it does not retain the exact segment-level
> churn-rate tables. Therefore, exact percentages for contract, tenure,
> senior-citizen, internet-service, security, support, and
> payment-method groups are intentionally not quoted here. Counts alone
> are not the same as within-group churn percentages.

## Visualizations

The notebook includes:

-   Overall churn count and percentage
-   Churn comparison by gender
-   Senior-citizen customer distribution and churn percentage
-   Tenure distribution by churn status
-   Churn comparison by contract type
-   Service-level comparisons for Phone Service, Multiple Lines,
    Internet Service, Online Security, Online Backup, Device Protection,
    Tech Support, Streaming TV, and Streaming Movies
-   Churn comparison by payment method

## Repository Structure

``` text
Customer-Churn-Analysis/
│
├── README.md
├── Customer Churn.csv
├── TCA.ipynb
└── Telco Customer Churn Analysis.pdf
```

## How to Run the Project

1.  Clone or download this repository.

2.  Make sure Python and Jupyter Notebook are installed.

3.  Install the required libraries:

    ``` bash
    pip install pandas numpy matplotlib seaborn jupyter
    ```

4.  Keep `Customer Churn.csv` in the same directory as `TCA.ipynb`.

5.  Open Jupyter Notebook and run the cells in `TCA.ipynb`.

## Future Improvements

-   Calculate and display exact churn rates for every customer segment.
-   Build an interactive dashboard using Power BI.
-   Perform statistical analysis to test relationships between customer
    attributes and churn.
-   Build a machine-learning classification model to predict customers
    at risk of churning.
-   Develop customer-retention recommendations based on model results.

## Conclusion

This exploratory analysis identifies several customer groups and service
characteristics associated with churn. Short-tenure customers,
month-to-month contract customers, customers without selected support
services, and electronic-check users deserve closer investigation. These
findings can help guide further analysis and the design of
customer-retention strategies.

------------------------------------------------------------------------

**Note:** This repository presents exploratory analysis, not a causal
study. Observed associations do not by themselves prove why a customer
churned.
