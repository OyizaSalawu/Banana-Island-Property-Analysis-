# Banana-Island-Property-Analysis-
This project presents an exploratory data analysis of residential properties in Banana Island, Lagos, conducted using Jupyter Lab. The dataset includes three properties, with analysis focused on occupancy trends, revenue, costs, and overall profitability.  The study identifies the best and worst performing months for each property.

This project provides a comprehensive financial and operational analysis of three distinct properties (Property A, B, and C) in Banana Island. Using Python, I modeled financial scenarios and identified operational trends to support data-driven investment decisions.
The analysis evaluates properties based on revenue performance, occupancy trends, and cost correlations over a 36-month period.

 Key Features:
Scenario Modeling: Calculation of "Worst Case," "Most Likely," and "Best Case" annual cash flows.
Occupancy Tracking: 36-month trend analysis of property usage.
Correlation Studies:Statistical analysis (Pearson coefficient) of the relationship between occupancy and operating costs.



💻 Key Implementation
Below are the core code snippets used to generate the financial models and correlation data.

1. Financial Scenario Modeling
I used the mean and standard deviation of daily revenue and occupancy to project annual performance.

```python
# Calculating the 'Best Case' scenario for Property C
# Formula: (Mean + Std Dev of Revenue) * (Mean + Std Dev of Occupancy) * 365
best_C = ((df_C['Daily_Revenue'].mean() + df_C['Daily_Revenue'].std()) * (df_C['Occupancy_Days'].mean() + df_C['Occupancy_Days'].std()) * 365)

print(f"Property C Best Case: {best_C.round(2)}")
```

2. Operational Cost Correlation
I analyzed whether a higher number of occupied days led to significantly higher monthly costs.

```python
# Checking correlation between Occupancy and Monthly Costs
correlation_A = property_A['Occupancy_Days'].corr(property_A['Monthly_Cost'])

print(f"Property A Correlation: {correlation_A:.2f}")
# Result: 0.23 (Weak positive correlation)
```



📈 Financial Performance Summary

 Property | Worst Case | Most Likely | Best Case |
Property A| 2,552,275.2 | 5,022,354.8 | 7,836,992.4 |
Property B| 3,504,875.9 | 5,305,782.1 | 7,305,016.7 |
Property C| 4,921,432.6 | 8,963,966.4 | 13,304,468.0 |

 
Higher occupancy levels lead to lower cost per use, showing that property profitability improves with increased utilization due to the distribution of fixed costs.
Property C outperforms others in revenue despite lower occupancy levels, suggesting that pricing and property value play a more critical role than occupancy alone. However, its high maintenance costs reduce overall profitability, emphasizing the need to balance premium pricing with cost efficiency.

Property C is the best performing property out of all three 




 🛠 Tools & Libraries
Python (Core Analysis)
Pandas & NumPy (Data Manipulation)
Matplotlib (Data Visualization)


