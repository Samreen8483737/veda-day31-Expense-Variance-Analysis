# Day 31: Expense Variance Analysis

## Objective
Execute a comprehensive Budget vs. Actual (BvA) analysis to evaluate departmental spending, calculate financial variances, and automatically flag material gaps requiring executive review.

## Technical Implementation
* **Data Engineering (Excel):** Processed the raw departmental budget dataset and engineered three critical calculated columns:
  * `Absolute_Variance`: Computed as `Actual - Budget` to capture raw dollar deviation.
  * `Variance_Percentage`: Computed as `(Actual - Budget) / Budget` to capture relative deviation.
  * `Material_Flag`: Implemented an `IF(ABS())` logic statement to automatically flag any departmental variance (over or under budget) exceeding a 10% threshold.
* **Business Intelligence (Power BI):** Developed an interactive financial dashboard to visualize the dataset.
  * Deployed KPI cards for macro-level tracking (Total Budget, Total Actuals, Total Variance).
  * Built a clustered bar chart for immediate visual identification of over-budget (Marketing & Ads) and under-budget (Travel & Entertainment) departments.
  * Constructed a detailed drill-down matrix with standardized financial formatting for granular review.

## Key Insights & Business Value
1. **Targeted Auditing:** The automated material flagging system successfully isolated "Marketing & Ads" (52.00% over budget) and "Travel & Entertainment" (56.25% under budget) as the primary drivers of corporate variance, allowing leadership to bypass noise and focus directly on problematic departments.
2. **Metric Integrity:** Validated the necessity of pairing absolute variance with percentage variance to ensure accurate scale context when presenting financial health to stakeholders.
